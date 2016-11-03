# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.
    Explain why each piece might be it's own component.

    ```md
    For example, if there is a list that has titles, and each titles have
    descriptions. We can represent visual hierarchies with nested components.
    Titles and description must be different components because we want to be
    able to first, see the titles of the items and then, click on them and see
    the description of each of those.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are
    their responsibilities?

    ```md
    component.js : actions for bindings can be set here
    template.hbs : we can add our handlebars and html here for a specific view state

    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that
    template?

    ```html
    {{#link-to 'my-contact' my-contact}} {{/link-to}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each my-contact.my-phone as |my-phone|}}
      {{#link-to 'my-phone' my-phone}}
      {{my-contact/my-phone my-phone=my-phone}}
      {{/link-to}}
    {{/each}}
    ```
