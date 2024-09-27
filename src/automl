from tpot import TPOTClassifier
from sklearn.model_selection import train_test_split

# Example data
X = movies_data[['Genres', 'Actors']]  # Features (in real-world you will have numerical encodings)
y = [5, 4, 3, 4, 5]  # Ratings

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

tpot = TPOTClassifier(verbosity=2, generations=5, population_size=20)
tpot.fit(X_train, y_train)

# Get the best model
print(tpot.fitted_pipeline_)