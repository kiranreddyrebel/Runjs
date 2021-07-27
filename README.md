# Coded by Tomnomnom
# Runjs
Tomnomnom's Prototype Pollution Scaning Tool


# Install

go get github.com/kiranreddyrebel/Runjs

# Recon Command

cat urls | unfurl -u format "%s://%d%p" | awk '{print $1 "?__proto__[foo]=bar"}' | ./Runjs -j 'window.foo? "vulnerable" : "not vulnerable"'
