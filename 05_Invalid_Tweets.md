- **Leetcode Problem No.** - 1683

- **Leetcode Link** - https://leetcode.com/problems/invalid-tweets/description
- **Problem statement** - Invalid Tweets
```
Table - Tweets
+----------------+---------+
| Column Name    | Type    |
+----------------+---------+
| tweet_id       | int     |
| content        | varchar |
+----------------+---------+
```
`tweet_id` is the primary key (column with unique values) for this table.
content consists of characters on an American Keyboard, and no other special characters.
This table contains all the tweets in a social media app.
 

Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.

Return the result table in any order.

**Solution** -
```
# Write your MySQL query statement below
SELECT
    tweet_id
FROM 
    Tweets
WHERE
    CHAR_LENGTH(content) > 15
```