# iChat Web Application

iChat is a real-time web chat application built with Flask and Socket.IO. It provides a seamless and interactive platform for users to communicate with each other through individual chat rooms.

## Project Structure

```
Chat_Web_App/
    myapp/
        static/
            images/
            auth.css
            chat.css
            index.js
            styles.css
        templates/
            auth.html
            base.html
            chat.html
            visualize.html
        __init__.py
        config.py
        database.py
        views.py
    .gitignore
    gunicorn_config.py
    README.md
    requirements.txt
    server.py
```

## Getting Started

To run the iChat web application locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Chat_Web_App.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up the environment variables:

   - Create a `.env` file in the project root.
   - Add the following lines to the `.env` file:

     ```env
     SECRET_KEY=your_secret_key_here
     DATABASE_URL=sqlite:///database.db
     ```

4. Run the server:

   ```bash
   python server.py
   ```
   or 
   ```bash
   gunicorn -c gunicorn_config.py server:app
   ```


Visit `http://localhost:5000` in your web browser to access iChat.

## Features

- **User Authentication:** Secure user registration and login with password hashing.
- **Real-time Chat:** Instant messaging in individual chat rooms.
- **Dynamic Chat List:** Automatically updates the chat list with new messages.
- **Responsive Design:** Works seamlessly on desktop and mobile devices.
- **Visualize User Registration Trends** Visualize the user registration data using Pandas and Matplotlib. This feature aims to analyze the number of users registered on the app over time and present the findings in a graphical format.

## Project Architecture

### `__init__.py`

Initialization of the Flask application, configuration, and extension setup.

### `config.py`

Configuration settings for the Flask application, including the secret key and database URI.

### `database.py`

Database models and schema definition using SQLAlchemy. Includes user, chat, and message models.

### `views.py`

Blueprint for route views, including login, registration, chat, and visualization routes.

### `gunicorn_config.py`

Gunicorn's configuration file for deployment settings.

### `server.py`

Entry point for running the server. Initializes the Flask application and Socket.IO communication events.

## ⛏️ Built With <a name = "tech_stack"></a>

<img alt="Flask" src="https://img.shields.io/badge/flask-%23000.svg?&style=for-the-badge&logo=flask&logoColor=white"/><img alt="HTML5" src="https://img.shields.io/badge/html5-%23E34F26.svg?&style=for-the-badge&logo=html5&logoColor=white"/><img alt="CSS3" src="https://img.shields.io/badge/css3-%231572B6.svg?&style=for-the-badge&logo=css3&logoColor=white"/><img alt="JavaScript" src="https://img.shields.io/badge/javascript-%23323330.svg?&style=for-the-badge&logo=javascript&logoColor=%23F7DF1E"/><img alt="Bootstrap" src="https://img.shields.io/badge/bootstrap-%23563D7C.svg?&style=for-the-badge&logo=bootstrap&logoColor=white"/><img alt="FlaskSqlalchemy" src ="https://img.shields.io/badge/FlaskSQLalchemy-%2307405e.svg?&style=for-the-badge&logo=sqlite&logoColor=white"/>

## 🤳 Screenshots <a name = "screenshots"></a>
|                                                                                                                                   |                                                                                                                                   |                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------:|
|  <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/register_login.png">  Register   |      <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/login_page.png" > Login      | <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/new_chat.png"> Add other users (Chat Window) |
| <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/chatting_1.png"> (Chat Window _A) | <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/chatting_2.png"> (Chat Window _B) |      <img width="1604" src="https://github.com/Adebowale-Morakinyo/Chat_Web_App/blob/main/Screenshot/chatting_3.png"> (Chat Window _C)       |
| <img width="1604" src="data:image/jpeg;base64,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"> (Chat Window _D) |

## Contributing

Contributions are welcome! If you'd like to contribute to iChat, please follow the [contribution guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE).

