# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.

---

# 📝 To-Do List App (React Native + Expo)

A simple and elegant **To-Do List mobile app** built with **React Native (Expo)**.
It allows users to **add, delete, mark as done**, and **search tasks** — with data **persisted locally** using AsyncStorage.

---

## 🚀 Features

- ✅ Add new tasks
- ✏️ Mark tasks as done / undone
- 🗑️ Delete tasks
- 🔍 Search through tasks instantly
- 💾 Persistent data storage (AsyncStorage)
- 📱 Beautiful and responsive UI

---

## 🛠️ Tech Stack

| Tool                    | Purpose                      |
| ----------------------- | ---------------------------- |
| **React Native (Expo)** | Mobile framework             |
| **TypeScript**          | Type safety                  |
| **AsyncStorage**        | Local data persistence       |
| **expo-checkbox**       | Task completion toggle       |
| **Ionicons**            | App icons                    |
| **SafeAreaView**        | Layout safety on all devices |

---

## 📂 Project Structure

```
📦 todo-app
 ┣ 📜 App.tsx / app/index.tsx      # Main app screen
 ┣ 📜 package.json
 ┣ 📜 tsconfig.json
 ┣ 📜 README.md
 ┗ 📂 assets                       # App images/icons
```

---

## ⚙️ Installation and Setup

1. **Clone the repository**

```bash
git clone https://github.com/DubTech-Web/my-to-do-list.git
cd todo-app
```

2. **Install dependencies**

```bash
npm install
# or
yarn install
```

3. **Start the app**

```bash
npx expo start
```

4. **Run on your device or emulator**

- Press **`a`** to open Android emulator
- Press **`i`** to open iOS simulator
- Or scan the **QR code** with the **Expo Go app**

---

## 💡 How It Works

- Tasks are stored as an array of objects in AsyncStorage under the key `"my-todo"`.
- When you open the app, tasks are loaded from storage.
- You can:

  - Add a new task using the bottom input field
  - Tap a checkbox to mark as done
  - Tap the trash icon 🗑️ to delete
  - Use the search bar to filter tasks

---

## 🧠 Code Highlights

### Task Type Definition

```ts
type ToDoType = {
  id: number;
  title: string;
  isDone: boolean;
};
```

### Add Task

```ts
const addTodo = async () => {
  const newTodo = { id: Math.random(), title: todoText, isDone: false };
  const updatedTodos = [...todos, newTodo];
  await AsyncStorage.setItem("my-todo", JSON.stringify(updatedTodos));
  setTodos(updatedTodos);
};
```

### Delete Task

```ts
const deleteTodo = async (id: number) => {
  const filtered = todos.filter((todo) => todo.id !== id);
  await AsyncStorage.setItem("my-todo", JSON.stringify(filtered));
  setTodos(filtered);
};
```

---

## 🧩 UI Overview

| Screen             | Description                      |
| ------------------ | -------------------------------- |
| 🏠 **Home Screen** | Displays list of todos           |
| ➕ **Add Task**    | Input field and button at bottom |
| 🔍 **Search Bar**  | Filters tasks dynamically        |
| ☑️ **Checkbox**    | Toggles task completion          |
| 🗑️ **Trash Icon**  | Deletes a task                   |

---

## 📸 Screenshots (Optional)

Add screenshots here if available:

```
📱 [ ] Home Screen
📱 [ ] Task Added
📱 [ ] Task Completed
```

---

🧩 Future Improvements

- Add **task details** (description, due date)
- Enable **edit existing task**
- Add **categories or priority levels**
- Use **SQLite** or **Firebase** for persistent cloud storage
- Add **dark mode**

---

👨🏽‍💻 Author

Enemuor Chidubem
💼 Built with ❤️ using React Native and Expo


---

.
