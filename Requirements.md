# Business process: *Increase Basket cost value by providing Delivery fee discount*

## Use case: *DD-1.1 - A Customer gets the discount after added new items in a basket*

### Functional Requirements

<table>
    <tr>
      <th>Code</th>
      <th>Name</th>
      <th>Description</th>
    </tr>
    <tr>
      <td>DD-1.1-1</td>
      <td>Settings for the discount</td>
      <td>User with Manager role must gets opportunity set up Target value of basket cost for Delivery fee discount, discount grid on Delivery Platform. Discount grid contains from values the settings above which correlates each other - if basket cost more then discount more. Max value of Delivery fee discount = 100%</td>
    </tr>
    <tr>
      <td>DD-1.1-2</td>
      <td>Consider the discount settings in algorithm of calculate basket cost value</td>
      <td>Delivery Platform must considers the discount settings (DD-1.1-1) in algorithm of calculate basket cost value. New algorithm TBD</td>
    </tr>
    <tr>
      <td>DD-1.1-3</td>
      <td>Suggestion discount for Customer</td>
      <td>Delivery Platform makes suggestion of Delivery fee discount to Customer by Mobile App. Suggestion appears per each Customer's order which reached Target basket cost for discount. Delivery Platform recalculate discount after each change of basket cost</td>
    </tr>
    <tr>
      <td>DD-1.1-4</td>
      <td>Dashboard for metrics of feature</td>
      <td>Reporting services should has a dashboard with business and technical metrics of feature. Metrics was describe in separate file "Metrics"</td>
    </tr>
</table>