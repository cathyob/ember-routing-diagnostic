# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Define the different 'pages' of the application (e.g. yesterday's lists, list, and list-edit)
    Provide preferred displayed URL paths (e.g. yesterday's '/lists/:list_id' and 'lists/:list_id/edit'})
    ```

2.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember generate route campus/boston
    ```

3.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    On the Boston campus' page you could put:
      {{#link-to 'campus'}}Back{{/link-to}}
    in order to allow the user to go back to the page of the list of campuses
    ```

4.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first route 1) nests the product within the products page directly 2) as a function
    The second route creates the route separately but makes it look like it is nested with the URL
    ```

5.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    I am not 100% sure about what this is asking - 123 must be a preestablished movie_id in order for it to be a valid route, otherwise it will load an error (e.g. blank page if situation not accounted for)
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Use an each to iterate through the data and build each model as an item on the page.
    ```
