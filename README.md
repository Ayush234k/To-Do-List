# To-Do-List

1. Overview :

This project is a simple to-do list application built using React. It allows users to manage a list of pages with descriptions and statuses. Users can add new pages, edit existing ones, and delete pages. The application uses modals for adding and editing pages, and displays the list in a table format.

2. System Design :

The application consists of three main components:

- **App (`App.jsx`)** : The main component that manages the overall state of the application, including:
        The list of tasks (stored in the `rows` state).
        Whether the modal is open or closed (`modalOpen` state).
        The index of the task being edited (`rowToEdit` state).

- **Modal (`Modal.jsx`)** : The modal dialog used for adding new tasks and editing existing ones. It handles the form input, validation, and submission.

- **Main (`Main.jsx`)** : This component displays the list of tasks in a table format. It receives the task data as a prop from the `App` component and allows you to edit or delete individual tasks.


3. Implementation :

State Management:** The application uses the `useState` hook to manage its state. The `App` component holds the main state, and the `Modal` component holds the state for the form.

Data Flow:** The data flows from the `App` component down to the `Main` and `Modal` components as props. Actions like adding, editing, and deleting tasks are handled in the `App` component, and the updated data is passed back down to the child components.

Form Handling:** The `Modal` component handles form input, validation, and submission. When the form is submitted, the `onSubmit` function in the `Modal` component calls the `handleSubmit` function in the `App` component, passing the task data.

Task Display:** The `Main` component renders the list of tasks in a table, using the `map` function to iterate over the `rows` array.


4. Setup and Running the Application :

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    ```

2.  **Install dependencies:**

    ```bash
    cd react-todo-list
    npm install
    ```

3.  **Start the development server:**

    ```bash
    npm start
    ```

The application will open in your browser at `http://localhost:3000`.
