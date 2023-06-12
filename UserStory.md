# Business process: *Increase Basket cost value by providing Delivery fee discount*

# User stories
### DD-1. **As** a customer of the Delivery service, **I want** get delivery fee discount **so that** a my order will be cheaper.  
*Note*: I always want to get most profitable suggestion on a market.

### DD-2. **As** a manager of the Delivery service, **I want** increase cost of orders **so that** it gets more revenue.  
*Note*: I keep track at a business metrics, and the revenue is one of them.

# Use cases
## DD-1.1 - A Customer gets the discount after added new items in a basket
<table>
    <tr>
      <td>Actors</td>
      <td>Customer, Delivery Platform, Mobile App</td>
    </tr>
    <tr>
      <td>Stackholders</td>
      <td>Manager</td>
    </tr>
    <tr>
      <td>Preconditions</td>
      <td>
      <ol>
        <li>
            Manager set minimal target value of basket cost for Delivery fee discount on Delivery platform
        </li>
        <li>
            Manager set values in discount grid on Delivery platform
        </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>Triggers</td>
      <td>Customer adds item in basket by Mobile App</td>
    </tr>
    <tr>
      <td>Main success scenario</td>
      <td>
        <ol>
            <li>Delivery Platform calculates Basket cost value</li>
            <li>Delivery Platform suggests to Customer adds new items in basket by Mobile App</li>
            <li>Customer adds new items within enough total cost in basket by Mobile App</li>
            <li>Delivery Platform calculates Delivery fee discount</li>
            <li>Customer creates order with Delivery fee discount by Mobile App </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>Alternative paths</td>
      <td>
      Alt case 1
      <ol start=3>
            <li>Customer ignores a suggest</li>
            <li>Customer creates order without Delivery fee discount by Mobile App </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>

## DD-1.2 - A Customer gets the discount after change quantity exists items in a basket
<table>
    <tr>
      <td>Actors</td>
      <td>Customer, Delivery Platform, Mobile App</td>
    </tr>
    <tr>
      <td>Stackholders</td>
      <td>Manager</td>
    </tr>
    <tr>
      <td>Preconditions</td>
      <td>
      <ol>
        <li>
            Manager set minimal target value of basket cost for the discount on the Delivery platform
        </li>
        <li>
            Manager set values in discount grid on Delivery platform
        </li>
        <li>
        There are quantity of items available for order
        </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>Triggers</td>
      <td>Customer adds item in basket by Mobile App</td>
    </tr>
    <tr>
      <td>Main success scenario</td>
      <td>
        <ol>
            <li>Delivery Platform calculates Basket cost value</li>
            <li>Delivery Platform suggests to Customer changes quantity of items in basket by Mobile App</li>
            <li>Customer increase quantity of items until enough total cost in basket by Mobile App</li>
            <li>Delivery Platform calculates Delivery fee discount</li>
            <li>Customer creates order with Delivery fee discount by Mobile App </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>Alternative paths</td>
      <td>
      Alt case 1
      <ol start=3>
            <li>Customer ignores a suggest</li>
            <li>Customer creates order without Delivery fee discount by Mobile App </li>
        </ol>
      Alt case 2
      <ol start=3>
            <li>Customer increase quantity of items in basket by Mobile App, but doesn't rich to enough total cost</li>
            <li>Delivery Platform suggests to Customer changes quantity of items in basket by Mobile App</li>
            <li>Customer ignores a suggest</li>
            <li>Customer creates order without Delivery fee discount by Mobile App </li>
        </ol>
        Alt case 3
      <ol start=3>
            <li>Customer increase quantity of items in basket by Mobile App, but doesn't rich to enough total cost</li>
            <li>Delivery Platform suggests to Customer changes quantity of items in basket by Mobile App</li>
            <li>Customer increase quantity of items until enough total cost in basket by Mobile App</li>
            <li>Customer creates order with Delivery fee discount by Mobile App </li>
        </ol>
      </td>
    </tr>
</table>

## DD-2.1 - The Delivery platform suggests the discount
<table>
    <tr>
      <td>Actors</td>
      <td>Manager, Delivery Platform</td>
    </tr>
    <tr>
      <td>Stackholders</td>
      <td>Customer</td>
    </tr>
    <tr>
      <td>Preconditions</td>
      <td>
      <ol>
        <li>
            A Manager set a target value of basket cost for the discount on the Delivery platform
        </li>
        <li>
            A Manager set a target revenue metric on the Delivery platform
        </li>
      </td>
    </tr>
    <tr>
      <td>Triggers</td>
      <td>A forecast of the revenue metric doesn't rich target value</td>
    </tr>
    <tr>
      <td>Main success scenario</td>
      <td>
        <ol>
            <li>Manager checks sign of revenue metric on Delivery Platform</li>
            <li>Manager activates discount program on Delivery Platform - Delivery fee discount from definition amount</li>
            <li>Delivery Platform suggests to groups of Customer Delivery fee discount from definition amount</li>
            <li>Delivery Platform periodical checks the revenue metric</li>
            <li>Delivery Platform gives sign of the change revenue metric</li>
            <li>Manager checks sign of revenue metric on Delivery Platform</li>
            <li>Manager deactivates a discount program on the Delivery Platform - Delivery fee discount from definition amount. If forecast of revenue metric has riched target value.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td>Alternative paths</td>
      <td>
      Alt case 1
      <ol start=7>
            <li>Manager leaves without changes launched discount program on the Delivery Platform - Delivery fee discount from definition amount. If forecast of revenue metric hasn't reached target value.</li>
        </ol>
        Alt case 2
      <ol start=2>
            <li>Delivery Platform automatically activates discount program - Delivery fee discount from definition amount</li>
            <li>Delivery Platform suggests to groups of Customer Delivery fee discount from definition amount</li>
            <li>Delivery Platform periodical checks the revenue metric</li>
            <li>Delivery Platform deactivates a discount program - Delivery fee discount from definition amount. If forecast of revenue metric has riched target value.</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
