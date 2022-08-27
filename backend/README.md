## GET /categories
  * Returns all the categories
  * URI:- http://127.0.0.1:5000/categories
  * Response
      ` {
      "categories": {
          "1": "history",
          "2": "science",
          "3" : "Geography",
          "4" : "History",
          "5" : "Entertainment",
          "6" : "Sports"
          },
      "success": true
          } `

## GET /questions
 * Returns all the questions in batches
 * URI:- http://127.0.0.1:5000/questions
 * Response 
    `{
        "categories": {
            "1": "Science",
            "2": "Art",
            "3": "Geography",
            "4": "History",
            "5": "Entertainment",
            "6": "Sports"
        },
        "questions": [
            {
            "answer": "Maya Angelou",
            "category": "4",
            "difficulty": 2,
            "id": 5,
            "question": "Whose autobiography is entitled 'I Know Why the Caged Bird Sings'?"
            },
            {
            "answer": "Edward Scissorhands",
            "category": "5",
            "difficulty": 3,
            "id": 6,
            "question": "What was the title of the 1990 fantasy directed by Tim Burton about a young man with multi-bladed appendages?"
            },
            {
            "answer": "Muhammad Ali",
            "category": "4",
            "difficulty": 1,
            "id": 9,
            "question": "What boxer's original name is Cassius Clay?"
            },
            {
            "answer": "Uruguay",
            "category": "6",
            "difficulty": 4,
            "id": 11,
            "question": "Which country won the first ever soccer World Cup in 1930?"
            },
            {
            "answer": "George Washington Carver",
            "category": "4",
            "difficulty": 2,
            "id": 12,
            "question": "Who invented Peanut Butter?"
            },
            {
            "answer": "Lake Victoria",
            "category": "3",
            "difficulty": 2,
            "id": 13,
            "question": "What is the largest lake in Africa?"
            },
            {
            "answer": "The Palace of Versailles",
            "category": "3",
            "difficulty": 3,
            "id": 14,
            "question": "In which royal palace would you find the Hall of Mirrors?"
            },
            {
            "answer": "Agra",
            "category": "3",
            "difficulty": 2,
            "id": 15,
            "question": "The Taj Mahal is located in which Indian city?"
            },
            {
            "answer": "Escher",
            "category": "2",
            "difficulty": 1,
            "id": 16,
            "question": "Which Dutch graphic artist\u2013initials M C was a creator of optical illusions?"
            },
            {
            "answer": "Mona Lisa",
            "category": "2",
            "difficulty": 3,
            "id": 17,
            "question": "La Giaconda is better known as what?"
            }
        ],
        "success": true,
        "total_questions": 24
      }`


## DELETE /questions/<int:id>
  * Deletes question with given ID.
  * URI:- http://127.0.0.1:5000/questions/12
  * Response
      ` {
              "id": 12,
              "message": "Question deleted successfully ",
              "success": true
          } `
## POST /questions
  * Inserting a new question.
  * URI:- http://127.0.0.1:5000/questions
  * JSON file format
      * {
          "answer": "blue",
          "category": "2",
          "difficulty": 1,    
          "id": 10,
          "question": "What is the colour of sky"
          }
  * Response
      ` {
          "question": {
              "answer": "blue",
              "category": "2",
              "difficulty": 1,
              "id": 17,
              "question": "What is the colour of sky"
                      },
          "success": true
       } `

## GET /categories/<int:category_id>/questions
  * Getting all question that belongs to a particular category
  * URI:- http://127.0.0.1:5000/categories/6/questions
  * Response
    ` {
    "questions": [
        {
        "answer": "Uruguay",
        "category": "6",
        "difficulty": 4,
        "id": 11,
        "question": "Which country won the first ever soccer World Cup in 1930?"
        }
    ],
    "success": true,
    "total_questions": 1
    } `

## GET /quizzes
  * Getting a random question within a choosen category
  * URI:- http://127.0.0.1:5000/quizzes
  * Response

## POST /questions  (SEARCH)
   * Takes in a search term, and returns all questions that matches the search term
   * URI:- http://localhost:5000/questions
   * Json format: 
     { "searchTerm": "soccer"}
   * Response 
     ` {
        "questions": [
            {
            "answer": "Brazil",
            "category": 6,
            "difficulty": 3,
            "id": 10,
            "question": "Which is the only team to play in every soccer World Cup tournament?"
            },
            {
            "answer": "Uruguay",
            "category": 6,
            "difficulty": 4,
            "id": 11,
            "question": "Which country won the first ever soccer World Cup in 1930?"
            }
        ],
        "totalQuestions": 2
        } `