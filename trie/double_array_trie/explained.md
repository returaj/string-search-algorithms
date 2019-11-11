## Double Array Trie:
#### Given data:
+ Total number of characters = 'N'
+ We also know all the integer representation of the characters (starting from 1 to N) 
+ list of words that is to be inserted in the trie 


#### 2 Dimentional Matrix Implementation:
+ Before we start to understand what double array trie is let start by looking at its naive implementation
  using a two dimensional matrix.
+ 2D Matrix size = N x N+1 (=> rows and column size is equal to the total number of characters 'N')
+ Why N x N+1 ?
  + Consider there are N (=5) characters arranged in row and column
  + Say word list = [ "ace$" , "bd$" , "ead$" ] (= where $ represent end of word ) 
  
    |     | a   | b   | c   | d   |  e  |  $  |
    | --- |---- | --- | --- | --- | --- | --- |
    |  a  |  0  |  0  |  1  |  1  |  0  |  0  |
    |  b  |  0  |  0  |  0  |  1  |  0  |  0  |
    |  c  |  0  |  0  |  0  |  0  |  1  |  0  |
    |  d  |  0  |  0  |  0  |  0  |  0  |  1  |
    |  e  |  1  |  0  |  0  |  0  |  0  |  1  |

  + a new character is created to represent end of word
  + Using 2D matrix we can store all the words. 
  + The above trie implementation is very fast but since the matrix is parse so it is not memory efficient.
  + We can compress rows using linked list but the find operation will be slow (O(n))

#### Triple Array Trie:
+ 
