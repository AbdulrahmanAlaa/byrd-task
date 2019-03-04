# byrd frontend developer task

## Brief
* Implement an invoice calculator, which will be used by the byrd staff to
  calculate and bill customers based on the number of orders processed.
* Scope
  * Use any language and framework of your choice
    * The byrd stack currently uses Angular (6)
  * Don't spend days working on your solution
    * **Focus on quality over quantity** - *production ready* code is preferred
    * If you run out of time, let us know what your solution is missing
* Submission
  * Send an email to `tech.careers@getbyrd.com`
  * Provide us with a link to your solution - e.g. GitHub, Bitbucket etc.
  * Provide a short explanation of your solution - e.g. the tools you used and why

## Workflow / User Journey
* On load, the user is presented with a form, which includes:
  * A customer selector (list retrieved from API)
  * A date range (start and end date)
* After submitting the form, the orders are retrieved from the API
* The page then displays the following:
  * A list of all the orders
    * The recipient name and email address
    * The total price of the order (based on the `total_price` from each item)
    * When the order was made
    * The items within the order
    * The delivery details
  * A summary at the top of the page
    * The date range and the total number of days
    * The total amount to invoice (based on the `charge_customer` value)
    * The number of orders

## API
* The API is documented and hosted on [Apiary](https://byrd1.docs.apiary.io/#)

### BONUS: State persistence
* Devise a way of storing the current state of the app, such that the user is
  able to refresh the page, and when the app reloads the previous state is
  displayed (i.e. including the state of the form and the orders retrieved)