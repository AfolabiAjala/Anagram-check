# Anagram-check
Given two strings, check to see if they are anagrams. An anagram is when the two strings can be written using the exact same letters (so you can just rearrange the letters to get a different phrase or word)


For example;
- 'A gentleman' is an anagram of 'Elegant man'
- 'Schoolmaster' is an anagram of 'The classroom'

### solution

```
def anagram2(w1,w2):
    
    # get rid of the white spaces and no space and set the strings to lower case
    w1 = w1.replace(' ', '').lower()
    w2 = w2.replace(' ', '').lower()
    
    # check if the lengths of both strings are equal
    if len(w1) != len(w2):
        return False
    
    # create a counter empty dictionary
    counter = {}
    
    for letter in w1:
        if letter in counter:
            counter[letter] += 1
        else:
            counter[letter] = 1
    
    for letter in w2:
        if letter in counter:
            counter[letter] -= 1
        else:
            counter[letter] = 1
            
    for i in counter:
        if counter[i] != 0:
            return False
    
    return True
    
  ```
