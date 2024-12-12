# Fall 2024 Principles of Databases — Assignment 4

* **Do not start this project until you’ve read and understood these instructions. If something is not clear, ask.**

---

## ❖ Introduction ❖

For this assignment, you will write responses to nine questions based on different topics from our textbook, *Database Systems — The Complete Book* and to one question based on your notes. Reply to each question in the provided region using Markdown syntax.

---

## ❖ Questions ❖

### 1. [2.4] What is the difference between a Cartesian Product, a Natural Join, and Theta-Joins?

**Cartesian product** is an algebraic operation that pairs every tuple from one relation every tuple in the second relation. The final relation contains every single tuple and attribute from both starting relations, but we resolve naming conflicts for similar attributes using dot notation (e.g., Relation1.AttributeName, Relation2.AttributeName). The resulting relation has a total number of tuples equal to (number of tuples in relation 1) × (number of tuples in relation 2). 

**Natural join** pairs tuples from two relations based on matching values in common attributes, keeping only the tuples that have matching values in the common attributes and eliminating duplicate columns for shared the attributes. 

**Theta joins** start with getting the cartesian product of the two relations, then applies a condition “theta” to filter the resulting combinations, the final relation only contains tuples that satisfy the condition requirements.

### 2. [2.5] What is a Referential Integrity Constraint?

Referential integrity constraint is expecting that a value in one relation's attribute must have a corresponding matching value in another relation's attribute. This can be applied across any attributes that are shared between two or more relations, but it is most commonly expected regarding foreign key creation, where every value that appears in a foreign key attribute must match a value in the referenced primary or unique key. Referential integrity constraints prevent “dangling tuples”, which are a pure violation of referential integrity, where a tuple in a foreign key does not match any values in the referenced relation. Overall, it ensures consistency of relations and validity of relationships. One way to apply referential integrity constraints to the database is to use the attribute-based `CHECK` constraints, for example:

```sql
foreign_key_attribute INT CHECK
    (foreign_key_attribute IN (SELECT primary_key_attribute FROM referenced_table))
```
This will reject any entry into the foreign key that does not match a value in the primary key.

Referential integrity constraints are expressed algebraically as:
π_attr1(relation1) ⊆ π_attr2(relation2)

###  3. [2.5] What is a Key Constraint?

Key constraints are when duplicate values in a key attribute are permitted if and only if the entire tuple is identical across all attributes. In other words, it is the same exact tuple just repeated. This also implies the other way around, meaning that no two different tuples are allowed to have the same value for key attribute. Key constraints ensure the uniqueness of tuples within the attribute that is specified as the key attribute.

### 4. [4.1] What is an Entity/Relationship Model? What purpose does it serve in the process of creating/designing databases?

Replace this content with your answer

### 5. [4.4] What is a Weak Entity Set?

Replace this content with your answer

### 6. [5.2.7; 6.3.8] Explain the concepts of Outerjoin, Natural Right Outer Joins, Natural Left Outer Joins, and Full Outer Joins.

Replace this content with your answer

### 7. [6.6.3] What is the difference between the SQL command `TRANSACTION` and the execution of any statement in SQL?

Replace this content with your answer

### 8. [8] What is a Virtual View and what are its advantages?

Replace this content with your answer

### 9. [8.3] What is an *index* and what are its advantages?

Replace this content with your answer

### 10. Explain the concept of an MVC, or model, view, controller, framework for designing full stack applications

Replace this content with your answer

---

## ❖ Due ❖

Sunday, 15 December 2024, at 10:00 AM.

---

## ❖ Grading ❖

| Item        | Points |
|-------------|:------:|
| Question 1  | `10`   |
| Question 2  | `10`   |
| Question 3  | `10`   |
| Question 4  | `10`   |
| Question 5  | `10`   |
| Question 6  | `10`   |
| Question 7  | `10`   |
| Question 8  | `10`   |
| Question 9  | `10`   |
| Question 10 | `10`   |

---

## ❖ Submission ❖

**NO late submissions will be accepted.**

You will need to issue a pull request back into the original repo, the one from which your fork was created for this project. See the **Issuing Pull Requests** section of [this site](http://code-warrior.github.io/tutorials/git/github/index.html) for help on how to submit your assignment.

**Note**: This assignment may **only** be submitted via GitHub. **No other form of submission will be accepted**.
