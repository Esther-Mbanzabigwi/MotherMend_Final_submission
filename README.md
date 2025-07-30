#  MotherMend Project

Wound Assistant is a comprehensive mobile application designed to assist in the assessment and management of C-section wounds. It leverages a machine learning model to classify wound types from images, providing valuable insights for healthcare professionals and patients.

The project is composed of three main components:

- **Backend**: A [Strapi](https://strapi.io/) application that serves as the API for the mobile app.
- **Frontend**: A [React Native](https://reactnative.dev/) (with [Expo](https://expo.dev/)) mobile application for iOS and Android.
- **ML Model**: A [PyTorch](https://pytorch.org/) model for wound classification, served via a [FastAPI](https://fastapi.tiangolo.com/) application.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation and Setup](#installation-and-setup)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
  - [ML Model Setup](#ml-model-setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Python](https://www.python.org/) (v3.9 or higher)
- [pip](https://pip.pypa.io/en/stable/)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Installation and Setup

### 1. Clone the Repository

First, clone the project repository to your local machine:

```bash
git clone <https://github.com/Esther-Mbanzabigwi/MotherMend_Final_submission.git>
cd <repository-directory>
```

### 2. Backend Setup

The backend is a Strapi application.

```bash
cd wound_assistant_backend/wound_assitant_backend
```

**Install dependencies:**

```bash
npm install
# or
yarn install
```

**Run the application:**

```bash
npm run develop
# or
yarn develop
```

The backend server will start on `https://wound-assitant-backend.onrender.com`.

### 3. Frontend Setup

The frontend is a React Native application built with Expo.

```bash
cd "wound_assistant_recovery-main (4)/wound_assistant_recovery-main"
```

**Install dependencies:**

```bash
npm install
# or
yarn install
```

**Start the application:**

```bash
npx expo start
```

This will open the Expo developer tools in your browser. You can then run the app on an Android emulator, iOS simulator, or on your physical device using the Expo Go app.

### 4. ML Model Setup

The machine learning model is served via a FastAPI application and is best run using Docker.

```bash
cd wound_classification_Model
```

**Build and run the Docker container:**

```bash
docker-compose up --build
```

The model's API will be available at `https://wound-model-api.onrender.com`. You can view the API documentation at `.

## Usage

Once all three components are running, you can use the mobile application to interact with the system. The mobile app will communicate with the backend for user management and data storage, and it will send images to the ML model for wound classification.

- **Backend API**: `https://wound-assitant-backend.onrender.com`
- **Frontend App**: Running via Expo Go or in an emulator.
- **ML Model API**: `https://wound-model-api.onrender.com`

## Project Structure

```
.
├── wound_assistant_backend/
│   └── wound_assitant_backend/  # Strapi backend
├── wound_assistant_recovery-main (4)/
│   └── wound_assistant_recovery-main/ # React Native (Expo) frontend
└── wound_classification_Model/    # FastAPI ML model
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request.

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
