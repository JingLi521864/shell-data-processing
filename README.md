# shell-data-processing

## Story
- This is an Tragedy of [Hamlet](http://shakespeare.mit.edu/hamlet/full.html). The story write by [Mr. William Shakespeare](https://en.wikipedia.org/wiki/William_Shakespeare).

## Process Text Data
- Now we'll use some Bash commands to process the text.
- Transform each space ' ' into a return character '\12' (aka ASCII line feed) [2]
  tr ' ' '\12' < returnedfile
- Pipe the output to sort (send the results of one command as input into another command)
  tr ' ' '\12' < returnedfile | sort
- Pipe the sorted output to uniq -c to count
  tr ' ' '\12' < returnedfile | sort | uniq -c
- Pipe the reduced output to sort with -nr flag
  tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr
- Redirect the output to result.txt
  tr ' ' '\12' < returnedfile | sort | uniq -c | sort -nr > result.txt

