README.md
Sometimes logs are overwhelming not because they’re complex,
but because they’re noisy.

This tiny script removes empty lines and repeated spaces
to make logs easier to scan with human eyes.

with open("input.log", "r") as f:
    lines = [line.strip() for line in f if line.strip()]

with open("cleaned.log", "w") as f:
    for line in lines:
        f.write(line + "\n")
