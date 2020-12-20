# Challenge Idea
We have an api that has random questions with multiple answers that need to fetch these questions to the client and ask him to answer these questions as showing each question as a single page `using vuejs route` 
> ex question 1: http://localhost/question/1
> ex question 2:http://localhost/question/2 ...etc 

After he answers all questions he can click the results button to view his points for each question `1 Point for each correct answer` and the total points
> ex: http://localhost/results

He can start over again with other questions.

Fllow this design by bootstrap:
[![1](https://optivius.com/s3/1.png)](https://optivius.com/s3/1.png)
[![1](https://optivius.com/s3/2.png)](https://optivius.com/s3/2.png)

##### Api schema is: 
### 
``` json
{
    "response_code": 0,
    "results": [
        {
            "category": "Category name",
            "type": "Type of question",
            "difficulty": "Question difficulty",
            "question": "The question in html encoded",
            "correct_answer": "The Correct answer in html encoded",
            "incorrect_answers": [ //Array Of the other incorrect Answers in html encoded
                "Answer 1",
                "Answer 2",
                "Answer 3"
            ]
        },
    ]
}
```
>> `Important:` You must view the correct answer with the incorrect answers in random position.

#### Api
``` code
https://opentdb.com/api.php?amount=10&category=18&difficulty=medium&type=multiple
```

## Acceptance Criteria
 - Client can’t access the results page until he answers all the questions.
 - Client can move forward and back between questions.
 - Each question must choose one answer only.
 - All used packages must be loaded from npm library.
 - Responsive

## Packages must use
- Vuejs
- bootstrap 4.5 or bootstrap-vue
- axios
- font-awesome (Optional) 

## The Evaluation
Task will be evaluated based on
1. Code quality
2. Application performance in slow network
3. Code scalability : ability to change type of category, difficulty and amount for questions in api
4. No errors on console
