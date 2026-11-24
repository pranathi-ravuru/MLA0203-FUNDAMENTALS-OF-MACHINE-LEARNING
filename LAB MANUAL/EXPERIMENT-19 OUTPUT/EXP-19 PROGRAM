from sklearn.naive_bayes import GaussianNB

X = [
    [50000, 750, 200000, 1],
    [60000, 800, 150000, 1],
    [25000, 550, 300000, 0],
    [30000, 600, 250000, 0],
    [70000, 780, 100000, 1],
    [20000, 500, 350000, 0],
    [65000, 820, 120000, 1],
    [28000, 580, 280000, 0]
]
y = [1, 1, 0, 0, 1, 0, 1, 0]

model = GaussianNB()
model.fit(X, y)

new_customer = [[55000, 770, 180000, 1]]

result = model.predict(new_customer)

print("Income:", new_customer[0][0])
print("Credit Score:", new_customer[0][1])
print("Loan Amount:", new_customer[0][2])
print("Employment (1=Yes):", new_customer[0][3])

if result[0] == 1:
    print("Loan Status: Approved")
else:
    print("Loan Status: Rejected")

print("Accuracy:", round(model.score(X, y) * 100, 2), "%")
