# Anagram-check
Given two strings, check to see if they are anagrams. An anagram is when the two strings can be written using the exact same letters (so you can just rearrange the letters to get a different phrase or word)


For example;
- 'A gentleman' is an anagram of 'Elegant man'
- 'Schoolmaster' is an anagram of 'The classroom'

### solution

```
def Anagram(w1,w2):
  #get rid of the white spaces and set to lower case
  
  w1 = w1.replace(' ','').lower()
  w2 = w2.replace(' ','').lower()
  
  #Check if the length of both strings are equal
  
  
  if len(w1) != len(w2):
    return False
  ```
