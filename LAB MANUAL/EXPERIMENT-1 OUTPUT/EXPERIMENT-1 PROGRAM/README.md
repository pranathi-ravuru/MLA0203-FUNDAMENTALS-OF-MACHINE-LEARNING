data = [
    ["Sunny", "Warm", "Normal", "Strong", "Warm", "Same", "Yes"],
    ["Sunny", "Warm", "High", "Strong", "Warm", "Same", "Yes"],
    ["Rainy", "Cold", "High", "Strong", "Warm", "Change", "No"],
    ["Sunny", "Warm", "High", "Strong", "Cool", "Change", "Yes"]
]


hypothesis = None

for row in data:
    attributes = row[:-1]
    target = row[-1]

    if target == "Yes":

        if hypothesis is None:
            hypothesis = attributes.copy()
        else:
            for i in range(len(hypothesis)):
                if hypothesis[i] != attributes[i]:
                    hypothesis[i] = "?"

print("Most Specific Hypothesis:")
print(hypothesis)
