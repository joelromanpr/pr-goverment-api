# Puerto Rico Government API

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An open-source API providing access to various public datasets from the Government of Puerto Rico. This project is intended for educational purposes, helping developers learn how to build applications that consume a RESTful API with real-world data.

## 📖 About The Project

The goal of this project is to provide a simple, stable, and easy-to-use data source for developers, students, and hobbyists. It's particularly useful for building educational apps, such as Android applications that demonstrate modern architecture patterns (MVVM, Repository) and showcase the capabilities of other open-source libraries like [`android-essentials-arch`](https://github.com/joel-pr/android-essentials-arch) or [`commandline-ktx`](https://github.com/joelromanpr/commandline-ktx).

## 🚀 Getting Started

You can start using the data immediately via our hosted endpoints or by cloning this repository and running it locally.

### Hosted API Endpoints (Recommended)

For your convenience, the data files are hosted on Firebase and are publicly accessible. This is the quickest way to integrate the data into your project.

#### ⚠️ Fair Use & Caching Policy
This API is hosted on a free plan. To ensure it remains available for everyone, please **cache the data on the client-side**. Do not fetch the data on every app start. A good practice is to fetch it once and store it in a local database (like Room on Android), refreshing it periodically (e.g., once a day).

---

### 1. Government Data

Provides a structured overview of the executive, legislative, and judicial branches of the Puerto Rico government.

*   **URL:** `https://pr-goverment-api.web.app/goverment.json`

<details>
  <summary>Click to see a sample of the JSON data</summary>

```json
{
  "executive_branch": {
    "governor": {
      "name": "Jenniffer González-Colón",
      "position": "Governor",
      "role_description": "The chief executive of Puerto Rico...",
      "party": "New Progressive Party (PNP)",
      "profile_picture_url": "..."
    },
    "cabinet": [
      {
        "role_description": "Acts as the Governor's chief of staff...",
        "position": "Secretary of State",
        "name": "To Be Announced",
        "party": "Non-partisan (Appointed)",
        "profile_picture_url": ""
      }
    ]
  }
}
```
</details>

### 2. Municipalities Data

A list of all 78 municipalities in Puerto Rico, including population, region, founding year, and historical context.

*   **URL:** `https://pr-goverment-api.web.app/municipalities.json`

<details>
  <summary>Click to see a sample of the JSON data</summary>

```json
[
  {
    "id": 1,
    "name": "San Juan",
    "region": "Metro",
    "population": 342259,
    "area_sq_mi": 76.93,
    "capital": true,
    "founding_year": 1521,
    "brief_history": "Founded by Juan Ponce de León...",
    "flag_url": "...",
    "seal_url": "..."
  }
]
```
</details>

### 3. Schools Data

A dataset of public schools, including location, type, student count, and special programs.

*   **URL:** `https://pr-goverment-api.web.app/schools.json`

<details>
  <summary>Click to see a sample of the JSON data</summary>

```json
[
  {
    "id": "school-001",
    "name": "Escuela Superior Central de Artes Visuales",
    "municipality": "San Juan",
    "district": "San Juan I",
    "type": "Public High School",
    "address": "Ave. Ponce de León #1500, San Juan, PR 00907",
    "student_count": 550,
    "programs": ["Visual Arts", "Performing Arts", "Music"],
    "latitude": 18.4480,
    "longitude": -66.0700
  }
]
```
</details>

---

## 💻 Local Development & Deployment

If you prefer to host the data yourself or wish to contribute, you can clone the repository and run a local server.

### Prerequisites

*   Node.js (LTS version recommended)
*   npm or yarn

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/your-username/pr-goverment-api.git
    ```
2.  Navigate into the project directory:
    ```sh
    cd pr-goverment-api
    ```
3.  Install the dependencies:
    ```sh
    npm install
    ```
4.  Start the local server:
    ```sh
    npm start
    ```
    The API will now be available at `http://localhost:3000`.

## 🙌 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**. Please feel free to fork the repo, create a feature branch, and open a pull request.

## 📄 License

Distributed under the MIT License. See the `LICENSE` file for more information.