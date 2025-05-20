# Flashcards

## Project Overview

**Flashcards** is a Redux-based quiz application built as part of the [Codecademy Front-End Engineer Career Path](https://www.codecademy.com/learn/front-end-engineer-career-path). This challenge marks the culmination of the **React Redux** module, offering hands-on experience in managing complex, interrelated state using Redux Toolkit.

The app allows users to:

- Create custom **topics** with icons.
- Add **quizzes** under specific topics.
- Define **flashcards** for each quiz with front and back content.
- Interact with quizzes by flipping cards to reveal answers.

## Technologies Used

- **React**: To build a component-based UI and manage local component state.
- **Redux & Redux Toolkit**: For managing global, structured state shared between features and components.
- **React Router**: For navigating between topics, quizzes, and forms.
- **JavaScript (ES6+)**: Core language for functionality and logic.
- **HTML & CSS**: For layout and styling.
- **uuid**: For generating unique IDs for topics, quizzes, and cards.
- **Git & GitHub**: For version control, collaboration, and deployment.

## Features

- **Create Topics**: Users can define new topics with a custom name and icon.
- **Create Quizzes**: Quizzes are associated with existing topics and support multiple cards.
- **Add Flashcards**: Each card includes a front and back, simulating a traditional flashcard.
- **Flip Cards**: Users can test themselves by flipping cards within a quiz.
- **Routing**: Page navigation is managed using `react-router-dom`.

## State Management Structure

The application follows a normalized Redux state pattern:

```js
{
  topics: {
    topics: {
      'topicId': {
        id: 'topicId',
        name: 'Topic Name',
        icon: 'URL',
        quizIds: ['quizId']
      }
    }
  },
  quizzes: {
    quizzes: {
      'quizId': {
        id: 'quizId',
        topicId: 'topicId',
        name: 'Quiz Name',
        cardIds: ['cardId1', 'cardId2']
      }
    }
  },
  cards: {
    cards: {
      'cardId1': {
        id: 'cardId1',
        front: 'Question',
        back: 'Answer'
      }
    }
  }
}
```

## Development Process

This project helped reinforce key Redux concepts, including:

- **Creating slices with `createSlice()`**
- **Connecting reducers to the store**
- **Dispatching actions and creating selectors**
- **Managing relationships across slices (e.g., quizzes belonging to topics)**

It took me three iterations before the concepts began to truly click. During this process, I also improved my **Git workflow** by creating feature branches for each slice (`topicsSlice`, `quizzesSlice`, `cardsSlice`) and merging only once each feature was complete and tested.

### Key Commits

```bash
feat: implement card state management and display
feat: handle state for creation of quizzes
feat: handle state for creation of topics
```

## Learnings and Reflections

- Gained deeper confidence in using **Redux Toolkit** and **managing normalized state**.
- Understood the importance of **data relationships** and **structuring app state**.
- Practiced **modular architecture** by splitting features into slices and organizing components by concern.
- Strengthened **Git practices**, especially around feature branching and clear commit messages.

## Setup and Installation

To run the project locally:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/SeanRavenhill/flashcards-react-redux.git
   cd flashcards-react-redux
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Start the development server**:

   ```bash
   npm start
   ```

4. **Open in browser**:
   Visit [http://localhost:3000](http://localhost:3000) to view the app.

## License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

## Acknowledgements

- Thanks to Codecademy for providing the project prompt and foundational starter code.
- Documentation and guidance from [Redux Toolkit](https://redux-toolkit.js.org/), [React Router](https://reactrouter.com/), and [uuid](https://www.npmjs.com/package/uuid).
