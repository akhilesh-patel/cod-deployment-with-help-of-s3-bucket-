
# Coding Standards

## Coding Style

* Follow C# coding standards provided by the .net runtime team:
  https://github.com/dotnet/runtime/blob/main/docs/coding-guidelines/coding-style.md

* Use a lint tool (static code analysis, at least for style) to help maintain standards across
  the whole codebase. Have a file in the project such as “.editorconfig” or “.prettier” to enforce the same style for all the developers.

* Have peer-review sessions regularly. 
  This will help to keep the style and improve some aspects of the code such as unit testing if a peer founds another case while reviewing a code made by someone else.

* Use meaningful descriptive words for the variables. Do not use abbreviations. Avoid single character variables like “i”, “x”. Always prefer “indexObjectName” or “tempObjectName” to improve readability.

* If a variable refers to a UI element, use prefixes to identify them. It can be a simple UI prefix like UIPhone, UIName or type specific UI prefix such as: TxtPhone, BtnConfirmation.

* Use spaces for indentation (not tabs). Can be 2 or 4 spaces but keep it consistent across the project.

* Avoid deep nesting.
* For react native development

        * Use TypeScript
        * Keep components small (consistent structure and use HOCs when possible and makes sense), 
          avoid excessive renders (use the memo APIs)

        * Lazy load components whenever possible to improve the app initial loading times.

        * Prefer FlatList over ScrollView for improved performance.
        * Enable Hermes for improved performance.

        * Have a clear design system. Use UI libraries, if possible, and extend them as needed. 
          Or build a custom and reusable component library to keep consistency across the app and maximize code reusability

        * Separate styles to their own file and maintain an easy-to-understand structure.

        * Use platform specific styles to maintain the native feel as much as possible.

        * Make sure to have breakpoints to allow for responsive mobile design.

        * Manage static image resources the right way: the image name require should be defined statically.
        
        * Use something like Sentry or Firebase Crashalytics for bugs and performance monitoring

        * Jest for unit testing.

        * Prefer functional components over class components for stateless. Try to keep components stateless.

        * Prefer to use state management tools such as MobX-state-tree or Redux instead of complex class components to manage states and have business logic.

        * If component needs to be stateful, and doesn’t keep track inside the state management tool, prefer class component over functional component (only case).

        * Lock dependencies when it makes sense to reduce risk of breaking changes when dependencies update.

        * Avoid loggers in Release Builds. Use something like Sentry or Firebase Crashalytics.
        * Use Safe Area View to guarantee compatibility with phones with a notch.
        * Define a folder structure and stick to it. Some common folders are: components, containers, api, hooks, store, navigation, i18n, screens, assets, utils, styles/theme.

# Programming Best Practices

* English is the official language for variable names and comments.
* Avoid writing very long methods. If a method has more than 30 lines of code (approximately) consider refactoring it to become multiple methods.
* Method name should be clear and tell exactly what it does. This helps reduce comments and increase readability.
* A method does “one job”. If two task are clearly identifiable in the same method, consider refactoring it into multiple methods.
* Always check for unexpected values to improve code stability.
* Formalize the use of try-catch-finally statements. Consider cases of software/network slowness before throwing errors and timeouts. Avoid empty catch blocks, at least log the error.
* Avoid hardcoded values as much as possible. Magic numbers should also be avoided, define constants at the top of the file or in another file and include it where needed. 
  Keep the values in resource files, especially strings that may change when localizing the software for the user.

* Have a good logging class.
* Error messages should always help the user solve the problem. Standardize error codes and provided meaningful information if possible. If the user can possibly fix the error themselves, provide a recommendation. 
  It not, tell them to contact support. Keep error messages short and concise for the user but be verbose in logs of the system to help reproduce and fix it.

# Architecture Best Practices
  * Always use N-Tier Architecture with at least three layers: Presentation, Logic, Data Layers. If possible, separate the Logic layer into Application Logic and Business Logic Layers.
  * Never access databases from UI code files. Always have a data layer class that performs the data related tasks.
  * Refactor code only when necessary and discuss it with peers and/or architect previously.

  * Follow the highly cohesive and loosely coupled principle as much as possible
  *  Manage infrastructure as code as much as possible.

  * Automate CI/CD tasks when possible and include testing.

  * Deploy code changes to new environments/containers each time the CI/CD pipeline runs.
  * Treat servers as stateless.

# Version Control Best Practices

  * Deliver code changes through git
  * Commit changes atomically
  * Clarity and completeness of commit messages
  * Tag releases
  * Branching strategy: It can be trunk based, release and feature branches, or git-flow. 
     The most important thing is to have it documented and stick to it. The idea of a good branching strategy is to optimize productivity,
     enable parallel development, allow structured releases, accommodate changes to be delivered asap, and support multiple versions of released software and patches.

  * Don´t break builds, i.e., have testing in place to avoid merging bad code back to the trunk/master branch.

  * Commit frequently, push at least once a day.
  * Security: make sure not to commit sensitive information to the version control system such as third-party secret keys.



## 🚀 About Me
I'm a full stack developer...



## Feedback

If you have any feedback, please reach out to us at fake@fake.com


# Hi, I'Kailash ! 👋


![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)


## Support

For support, email fake@fake.com or join our Slack channel.


## Run Locally

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```


## Running Tests

To run tests, run the following command

```bash
  npm run test
```





## Deployment

To deploy this project run

```bash
  npm run deploy
```


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Authors

- [@octokatherine](https://www.github.com/octokatherine)


## Documentation

[Documentation](https://linktodocumentation)


## Usage/Examples

```javascript
import Component from 'my-project'

function App() {
  return <Component />
}
```

