- **Leetcode Problem No.** - 1148

- **Leetcode Link** - https://leetcode.com/problems/article-views-i/description
- **Problem statement** - Article Views 1
```
Table - Views
+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| article_id    | int     |
| author_id     | int     |
| viewer_id     | int     |
| view_date     | date    |
+---------------+---------+
```
There is no primary key (column with unique values) for this table, the table may have duplicate rows.
Each row of this table indicates that some viewer viewed an article (written by some author) on some date. 
Note that equal `author_id` and `viewer_id` indicate the same person.
 

Write a solution to find all the authors that viewed at least one of their own articles.

Return the result table sorted by id in ascending order.

**Solution** -
```
# Write your MySQL query statement below
SELECT 
    DISTINCT(author_id) as id
FROM
    Views
WHERE
    author_id = viewer_id
ORDER BY 1
```