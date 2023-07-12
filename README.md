<div align="center">
<h1 align="center">
<img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100" />
<br>local-weather
</h1>
<h3>◦ Stay informed, rain or shine!</h3>
<h3>◦ Developed with the software and tools listed below.</h3>

<p align="center">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E.svg?style&logo=JavaScript&logoColor=black" alt="JavaScript" />
<img src="https://img.shields.io/badge/HTML5-E34F26.svg?style&logo=HTML5&logoColor=white" alt="HTML5" />
<img src="https://img.shields.io/badge/PostCSS-DD3A0A.svg?style&logo=PostCSS&logoColor=white" alt="PostCSS" />
<img src="https://img.shields.io/badge/Autoprefixer-DD3735.svg?style&logo=Autoprefixer&logoColor=white" alt="Autoprefixer" />
<img src="https://img.shields.io/badge/Vite-646CFF.svg?style&logo=Vite&logoColor=white" alt="Vite" />

<img src="https://img.shields.io/badge/Axios-5A29E4.svg?style&logo=Axios&logoColor=white" alt="Axios" />
<img src="https://img.shields.io/badge/Vue.js-4FC08D.svg?style&logo=vuedotjs&logoColor=white" alt="Vue.js" />
<img src="https://img.shields.io/badge/Markdown-000000.svg?style&logo=Markdown&logoColor=white" alt="Markdown" />
<img src="https://img.shields.io/badge/JSON-000000.svg?style&logo=JSON&logoColor=white" alt="JSON" />
</p>
<img src="https://img.shields.io/github/languages/top/ehte92/local-weather?style&color=5D6D7E" alt="GitHub top language" />
<img src="https://img.shields.io/github/languages/code-size/ehte92/local-weather?style&color=5D6D7E" alt="GitHub code size in bytes" />
<img src="https://img.shields.io/github/commit-activity/m/ehte92/local-weather?style&color=5D6D7E" alt="GitHub commit activity" />
<img src="https://img.shields.io/github/license/ehte92/local-weather?style&color=5D6D7E" alt="GitHub license" />
</div>

---

## 📒 Table of Contents

- [📒 Table of Contents](#-table-of-contents)
- [📍 Overview](#-overview)
- [⚙️ Features](#️-features)
- [📂 Project Structure](#-project-structure)
- [🧩 Modules](#-modules)
- [🚀 Getting Started](#-getting-started)
  - [📦 Installation](#-installation)
  - [🎮 Using local-weather](#-using-local-weather)
  - [🧪 Compile and Minify for Production](#-compile-and-minify-for-production)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 📍 Overview

The project is a weather application that allows users to search for cities and track their weather information. It provides real-time weather updates, including current weather conditions, hourly forecasts, and 7-day forecasts. The app aims to provide users with a seamless and intuitive experience for quickly accessing and staying informed about the weather in their desired locations. This value proposition makes it a valuable tool for planning activities, travel, and staying prepared for weather changes.

---

## ⚙️ Features

| Feature              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **⚙️ Architecture**  | The codebase follows a modern front-end architecture using Vue.js as the main framework. The project is structured as a single-page application (SPA) with multiple components and views. It adopts a component-based architecture, separating the application into reusable and self-contained components, such as CityView, SiteNavigation, CityCard, etc. The Vue Router is used for navigation between different views. The architecture allows for easy reusability, maintainability, and scalability of the codebase.                                                                      |
| **📖 Documentation** | The repository lacks comprehensive documentation. Although some files have code comments explaining their purpose and functionality, there is no centralized documentation or README file explaining the project's overall structure, setup instructions, or usage guidelines. This can make it challenging for new developers to understand and contribute to the project. Improved documentation would greatly benefit the project's usability and onboarding process.                                                                                                                         |
| **🔗 Dependencies**  | The project relies on several external dependencies, such as Vue.js, Tailwind CSS, and Font Awesome. Vue.js is a widely-used JavaScript framework for building user interfaces, providing the core functionality of the application. Tailwind CSS is a utility-first CSS framework used for styling the components. Font Awesome provides a library of icons used in the project. The dependencies are managed using npm and can be found in the package.json file. The project also relies on external APIs, such as OpenWeatherMap and Mapbox, to fetch weather data and search for locations. |
| **🧩 Modularity**    | The codebase demonstrates good modularity by organizing the project into smaller, reusable components. Each component is responsible for a specific part of the application's functionality, such as displaying weather information, handling navigation, or rendering placeholders. This modular approach allows developers to understand and modify specific parts of the application without affecting others, enhancing code maintainability. However, further modularization could be achieved by extracting common functionality into shared modules, reducing code duplication.           |
| **✔️ Testing**       | The codebase does not include any explicit tests. Lack of tests can make it difficult to ensure the reliability and correctness of the application. Implementing a comprehensive testing strategy, such as unit tests for individual components and integration tests for the overall functionality, would improve the quality and stability of the code. Popular testing frameworks for Vue.js applications include Jest and Vue Test Utils, which could be considered for future test implementation.                                                                                          |
| **⚡️ Performance**  | The project does not present any obvious performance issues. However, performance optimization techniques, such as lazy loading of resources, code splitting, and caching, could be implemented to enhance the loading speed and overall performance of the application. Additionally, minimizing the use of heavy external libraries or optimizing API calls can further improve performance. Monitoring tools like Lighthouse or WebPagetest can be used to                                                                                                                                    |

---

## 📂 Project Structure

---

## 🧩 Modules

<details closed><summary>Root</summary>

| File                                                                                       | Summary                                                                                                                                                                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [index.html](https://github.com/ehte92/local-weather/blob/main/index.html)                 | The provided code snippet is an HTML file that sets up the basic structure and includes necessary dependencies for a web application. It imports a JavaScript file called "main.js" and renders the application within a div element with the id "app". It also includes font styles from Google Fonts and icons from Font Awesome. |
| [tailwind.config.js](https://github.com/ehte92/local-weather/blob/main/tailwind.config.js) | The code snippet is a configuration file for Tailwind CSS. It defines the content to be processed, extends the theme with custom colors and font, sets container properties, and defines screen sizes.                                                                                                                              |
| [vite.config.js](https://github.com/ehte92/local-weather/blob/main/vite.config.js)         | This code snippet is a Vite configuration file. It imports the necessary modules, such as `node:url`, `vite`, and `vue`. It defines a Vite configuration using the `defineConfig` function. It includes a Vue plugin and resolves aliases for the `@` symbol to the `src` directory.                                                |
| [postcss.config.js](https://github.com/ehte92/local-weather/blob/main/postcss.config.js)   | The code snippet exports a module that contains two plugins: tailwindcss and autoprefixer. These plugins are typically used in a build process to process and optimize CSS stylesheets, including adding vendor prefixes and applying utility classes.                                                                              |

</details>

<details closed><summary>Src</summary>

| File                                                                     | Summary                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [App.vue](https://github.com/ehte92/local-weather/blob/main/src/App.vue) | The code snippet is a Vue template that sets up the basic structure of a website. It includes a site navigation component, a router view to dynamically render components, and a transition for smooth page transitions. The code also imports necessary dependencies and defines some styling. |
| [main.js](https://github.com/ehte92/local-weather/blob/main/src/main.js) | This code snippet sets up a Vue app with a router, mounts it to an HTML element with the id "app", and imports a Tailwind CSS file for styling.                                                                                                                                                 |

</details>

<details closed><summary>Components</summary>

| File                                                                                                                | Summary                                                                                                                                                                                                                                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CityViewSkeleton.vue](https://github.com/ehte92/local-weather/blob/main/src/components/CityViewSkeleton.vue)       | The code snippet defines a template in Vue.js that displays multiple instances of an AnimatedPlaceholder component. The placeholders are rendered in different sections of the page, including an overview section, an hourly section, and a weekly section. The code also imports the AnimatedPlaceholder component from another file.                                                             |
| [SiteNavigation.vue](https://github.com/ehte92/local-weather/blob/main/src/components/SiteNavigation.vue)           | This code snippet is a Vue component that represents the header section of a weather application. It includes navigation links, a modal for displaying information about the application, and functionality for adding cities to track their weather. The code utilizes Vue Router for navigation and localStorage for saving city data.                                                            |
| [BaseModal.vue](https://github.com/ehte92/local-weather/blob/main/src/components/BaseModal.vue)                     | This code snippet defines a modal component that can be used to display a modal dialog. It utilizes Vue's teleport feature to render the modal outside of its current component's DOM hierarchy. The modal is shown when the "modalActive" prop is true, and it can be closed by emitting a "close-modal" event. The code also includes CSS transitions for the modal's enter and leave animations. |
| [AsyncCityView.vue](https://github.com/ehte92/local-weather/blob/main/src/components/AsyncCityView.vue)             | This code snippet is a Vue component that displays weather information for a specified city. It retrieves weather data from the OpenWeatherMap API using the provided latitude and longitude. The component shows the current weather, hourly weather forecast, and a 7-day forecast. It also allows users to remove the city from their saved cities list.                                         |
| [CityCard.vue](https://github.com/ehte92/local-weather/blob/main/src/components/CityCard.vue)                       | This code snippet is a Vue.js component that displays weather information for a given city. It takes a "city" object as a prop and renders the city name, state, current temperature, and daily temperature range. The temperatures are rounded to the nearest degree. The component is designed with responsive styling and cursor interaction.                                                    |
| [CityList.vue](https://github.com/ehte92/local-weather/blob/main/src/components/CityList.vue)                       | This code snippet renders a list of saved cities, displaying their weather information. It fetches weather data from an API and updates the savedCities array with the fetched data. Clicking on a city card navigates to a detailed view of that city.                                                                                                                                             |
| [AnimatedPlaceholder.vue](https://github.com/ehte92/local-weather/blob/main/src/components/AnimatedPlaceholder.vue) | The code snippet is a Vue.js template that creates a div element with a pulsating animation effect and a gradient background color that transitions from gray to white.                                                                                                                                                                                                                             |
| [CityCardSkeleton.vue](https://github.com/ehte92/local-weather/blob/main/src/components/CityCardSkeleton.vue)       | The provided code snippet is a template that displays a styled container with four instances of a component called "AnimatedPlaceholder". The placeholders are arranged in two columns, with each column containing two placeholders. The component is imported from another file called "AnimatedPlaceholder.vue".                                                                                 |

</details>

<details closed><summary>Views</summary>

| File                                                                                     | Summary                                                                                                                                                                                                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [CityView.vue](https://github.com/ehte92/local-weather/blob/main/src/views/CityView.vue) | This code snippet sets up a template for a Vue.js component. It imports two components, AsyncCityView and CityViewSkeleton. The code uses the Suspense component to render the AsyncCityView component, and if it takes too long to load, it shows the CityViewSkeleton component as a fallback.                                                                                                              |
| [HomeView.vue](https://github.com/ehte92/local-weather/blob/main/src/views/HomeView.vue) | The code snippet initializes a Vue script that handles a search feature for cities and states. It uses the Mapbox API to fetch search results based on the user's input and displays them in a dropdown list. The selected city is then used to navigate to a separate route, passing relevant parameters. Additionally, the code includes components for displaying a list of cities and a loading skeleton. |

</details>

<details closed><summary>Router</summary>

| File                                                                              | Summary                                                                                                                                                                                                                                                               |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [index.js](https://github.com/ehte92/local-weather/blob/main/src/router/index.js) | This code snippet sets up the Vue router with two routes-one for the home page and one for displaying weather information for a specific city. It also includes a navigation guard that updates the document title based on the route parameters or meta information. |

</details>

---

## 🚀 Getting Started

### 📦 Installation

1. Clone the local-weather repository:

```sh
git clone https://github.com/ehte92/local-weather
```

2. Change to the project directory:

```sh
cd local-weather
```

3. Install the dependencies:

```sh
`ℹ️  npm install`
```

### 🎮 Using local-weather

```sh
`ℹ️  npm run dev`
```

### 🧪 Compile and Minify for Production

```sh
`ℹ️  npm run build`
```

---

## 🤝 Contributing

Contributions are always welcome! Please follow these steps:

1. Fork the project repository. This creates a copy of the project on your account that you can modify without affecting the original project.
2. Clone the forked repository to your local machine using a Git client like Git or GitHub Desktop.
3. Create a new branch with a descriptive name (e.g., `new-feature-branch` or `bugfix-issue-123`).

```sh
git checkout -b new-feature-branch
```

4. Make changes to the project's codebase.
5. Commit your changes to your local branch with a clear commit message that explains the changes you've made.

```sh
git commit -m 'Implemented new feature.'
```

6. Push your changes to your forked repository on GitHub using the following command

```sh
git push origin new-feature-branch
```

7. Create a new pull request to the original project repository. In the pull request, describe the changes you've made and why they're necessary.
   The project maintainers will review your changes and provide feedback or merge them into the main branch.

---

## 📄 License

This project is licensed under the `ℹ️  INSERT-LICENSE-TYPE` License. See the [LICENSE](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository) file for additional info.

---
