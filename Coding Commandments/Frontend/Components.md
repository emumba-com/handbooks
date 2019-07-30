# Categorize By Type
In a typical project, you can have two types of components:
- Those which represent a full page against a URL. Such components aren't expected to be re-used at multiple instances. They can be placed under `src/routes` directory.
- Those which represent a widget that can be re-used across multiple pages. Such components can be placed under `src/components` directory.

# Use Nouns for Names
Use nouns for naming your components. Nouns, in English language, refer to names of things. For example, `Emumba` is a noun, or `Phone` is a noun. Learn more about nouns from this [short video](https://www.khanacademy.org/humanities/grammar/parts-of-speech-the-noun/grammar-nouns/v/introduction-to-nouns-the-parts-of-speech-grammar-khan-academy).

# Give A Directory To Each Component
Wrap each component's resources inside its own directory. For example, a component `Header.js` can be placed inside `src/components/Header`, along with its dependent files such as `Header.scss` etc.

# Be Dumb
Begin writing a React component as a [dumb component](https://medium.com/@thejasonfile/dumb-components-and-smart-components-e7b33a698d43) (a function based component). Convert it to a smart component (a class based component) only if you need either component state, or lifecycle hooks.

# Avoid State
Avoid using state within components as much as possible. Use component state only when there is some information that's very local to the component itself, for example, toggle state of a drop down component. Use Redux for all other scenarios.

# Localize Styling
Avoid using global styles for a component. Create each component's style file along with it, with the same name. For example, you can have `Header.scss` for a component `Header.js`. Use [CSS Modules](https://github.com/css-modules/css-modules) in the style files, so there are no namespace conflicts.