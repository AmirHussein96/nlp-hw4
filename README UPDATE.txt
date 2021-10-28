Hi Amir,

There are still a few bugs we have to work out:

parse_amir.py that you just pushed works on the arith grammar, but not on the papa grammar or the wallstreet grammar.

parse_amir_Wednesday.py is the previous version from earlier on Wednesday. It works on papa and wallstreet but not on arith.

I have added the print function to both (still some bugs to fix, but its late).
I only added the speedup to _Wednesday because we should submit the slow and fast versions separately. The first speedup is 3 lines, easy to add.

There are a few issues with the printing in parse_amir_Wednesday:
1. some test sentences work fine, but it gets an error with sentence: 
	"Papa ate the caviar with a spoon"
because the node for S -> NP VP only has one child, VP. There is no child for the NP constituent.

2. We hit a max recursion depth on wallstreet.gr. Its too late for me to be able to work it out right now.