<<<<<<< HEAD
In this project, let's build a **Nxt Trendz - Cart Features** by applying the concepts we have learned till now.

### Refer to the video below:

<br/>
<div style="text-align: center;">
  <video style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12);outline:none;" loop="true" autoplay="autoplay" controls="controls" muted>
    <source src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-output.mp4" type="video/mp4">
  </video>
=======
In this project, let's build an **IPL Dashboard App** by applying the concepts we have learned till now.

### Refer to the image below:

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-output-v2.gif" alt="ipl-dashboard-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7
</div>
<br/>

### Design Files

<details>
<summary>Click to view</summary>

<<<<<<< HEAD
- [Extra Small (Size < 576px) and Small (Size >= 576px)](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-sm-output-v0.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px)](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-lg-output.png)
=======
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Home](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-home-sm-output.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Team Matches](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-team-matches-sm-output-v2.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-home-lg-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Team Matches](https://assets.ccbp.in/frontend/content/react-js/ipl-dashboard-team-matches-lg-output-v2.png)
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Completion Instructions

<details>
<summary>Functionality to be added</summary>
<br/>

The app must have the following functionalities

<<<<<<< HEAD
- When an unauthenticated user tries to access the **Cart** Route, then the page should be navigated to **Login** Route

- Following are the features to be implemented

  - Feature 1

    - When an authenticated user tries to add the same product multiple times
      - The quantity of the product should be updated accordingly, and the count of the cart items in the header should be remained same

  - Feature 2

    - The total amount and number of items in the cart should be displayed in the **Cart** Route

  - Feature 3

    - In each cart item in the cart
      - When the plus icon is clicked, then the quantity of the product should be incremented by one
      - When the minus icon is clicked, then the quantity of the product should be decremented by one
      - When the quantity of the product is one and the minus icon is clicked, then the respective product should be removed from the cart
      - Based on the quantity of the product, the product price and the Cart Summary, i.e the total cost should be updated accordingly

  - Feature 4

    - When an authenticated user clicks on the remove button, cart item should be removed from the cart list

  - Feature 5

    - When an authenticated user clicks on the **Remove All** button, all the cart items should be removed from the cart and [Empty Cart View](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-empty-cart-view.png) should be displayed

- The `CartContext` has an object as a value with the following properties
  - `cartList` - this key stores the cart items
  - `removeAllCartItems` - this method is used to remove all the cart items in the `cartList`
  - `addCartItem` - this method adds the cart item to the `cartList`
  - `removeCartItem` - this method removes the cart item from the `cartList`
  - `incrementCartItemQuantity` - this method increases the quantity of a product in the `cartList`
  - `decrementCartItemQuantity` - this method decreases the quantity of a product in the `cartList`
=======
- When the app is opened, Home Route should be displayed
- When the Home Route is opened,
  - Make HTTP GET request to the **teamsApiUrl**
  - **_loader_** should be displayed while fetching the data
  - After fetching the data, the list of teams should be displayed
- When a team card in Home Route is clicked,
  - Page should be navigated to the Team Matches Route with the URL `/team-matches/:id`
- When the Team Matches Route is opened,
  - Make HTTP GET request to the **teamMatchesApiUrl** with the team id to get the recent matches data of the team
    - Example: `https://apis.ccbp.in/ipl/KKR`
  - **_loader_** should be displayed while fetching the data
  - After fetching the data, the team banner, latest match, and list of recent matches should be displayed

</details>

<details>

<summary>API Requests & Responses</summary>
<br/>

**teamsApiUrl**

#### API: `https://apis.ccbp.in/ipl`

#### Method: `GET`

#### Description:

Returns a response containing the list of all IPL teams

#### Response

```json
{
  "teams": [
    {
      "name": "Royal Challengers Bangalore",
      "id": "RCB",
      "team_image_url": "https://assets.ccbp.in/frontend/react-js/rcb-logo-img.png",
      // use value of the key 'name' for alt as `${name}`
    },
    ...
  ],
}
```

**teamMatchesApiUrl**

#### API: `https://apis.ccbp.in/ipl/:id`

#### Example: `https://apis.ccbp.in/ipl/KKR`

#### Method: `GET`

#### Description:

Returns a response containing details of all recent matches of a team

#### Response

```json
{
  "team_banner_url": "https://assets.ccbp.in/frontend/react-js/kkr-team-img.png",
  "latest_match_details": {
    "umpires": "CB Gaffaney, VK Sharma",
    "result": "Kolkata Knight Riders Won by 7 wickets",
    "man_of_the_match": "Shubman Gill",
    "id": "1216545",
    "date": "2020-09-26",
    "venue": "At Sheikh Zayed Stadium, Abu Dhabi",
    "competing_team": "Sunrisers Hyderabad",
    "competing_team_logo": "https://upload.wikimedia.org/wikipedia/en/thumb/8/81/Sunrisers_Hyderabad.svg/1200px-Sunrisers_Hyderabad.svg.png",
    // use value of the key 'competing_team' for alt as `latest match ${competing_team}`
    "first_innings": "Sunrisers Hyderabad",
    "second_innings": "Kolkata Knight Riders",
    "match_status": "Won",
  },
  "recent_matches": [
    {
      "umpires": "RK Illingworth, K Srinivasan",
      "result": "Royal Challengers Bangalore Won by 82 runs",
      "man_of_the_match": "AB de Villiers",
      "id": "1216540",
      "date": "2020-10-12",
      "venue": "At Sharjah Cricket Stadium, Sharjah",
      "competing_team": "Royal Challengers Bangalore",
      "competing_team_logo": "https://upload.wikimedia.org/wikipedia/en/thumb/2/2a/Royal_Challengers_Bangalore_2020.svg/1200px-Royal_Challengers_Bangalore_2020.svg.png",
      // use value of the key 'competing_team' for alt as `competing team ${competing_team}`
      "first_innings": "Royal Challengers Bangalore",
      "second_innings": "Kolkata Knight Riders",
      "match_status": "Lost",
    },
    ...
  ],
}
```
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
<<<<<<< HEAD
    <img src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-component-structure-breakdown.png" alt="component structure breakdown" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
=======
    <img src="https://assets.ccbp.in/frontend/content/react-js/home-component-structure-img.png" alt="home component structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/team-matches-component-structure-img.png" alt="team matches component structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7
</div>
<br/>

</details>

<details>
<summary>Implementation Files</summary>
<br/>

Use these files to complete the implementation:

- `src/App.js`
<<<<<<< HEAD
- `src/components/Cart/index.js`
- `src/components/Cart/index.css`
- `src/components/CartItem/index.js`
- `src/components/CartItem/index.css`
- `src/components/CartSummary/index.js`
- `src/components/CartSummary/index.css`
=======
- `src/components/Home/index.js`
- `src/components/Home/index.css`
- `src/components/TeamCard/index.js`
- `src/components/TeamCard/index.css`
- `src/components/TeamMatches/index.js`
- `src/components/TeamMatches/index.css`
- `src/components/LatestMatch/index.js`
- `src/components/LatestMatch/index.css`
- `src/components/MatchCard/index.js`
- `src/components/MatchCard/index.css`
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7
</details>

### Quick Tips

<details>
<summary>Click to view</summary>
<br>

<<<<<<< HEAD
- The `line-height` CSS property sets the height of a line box. It's commonly used to set the distance between lines of text

  ```
  line-height: 1.5;
  ```

    <br/>
    <img src="https://assets.ccbp.in/frontend/react-js/line-height-img.png" alt="line height" style="width:90%; max-width: 600px;"/>

- The array method `find()` returns the first item's value that satisfies the provided testing function. If no item is found, it returns `undefined`

  **Syntax**: `arr.find(Testing Function)`
=======
- To display the animated loader, we need to import the Loader component using the below statement

  ```
  import Loader from 'react-loader-spinner'
  ```

- In order to display the given animated loader, pass the `type` and `color` props to the `Loader` component with values as **Oval** and **#ffffff** , respectively

  ```
  <Loader type="Oval" color="#ffffff" height={50} width={50} />
  ```
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

**The following instructions are required for the tests to pass**

<<<<<<< HEAD
- `BsPlusSquare`, `BsDashSquare` icons from `react-icons` should be used for **plus** and **minus** buttons in cart item
- The Cart Item should consist of two HTML button elements with data-testid attribute values as **plus** and **minus** respectively
- `AiFillCloseCircle` icon from react-icons should be used for **remove** button in cartItem
- The Cart Item should consist of an HTML button element with data-testid attribute values as **remove**
- The product image in **Cart Item** Route should have the alt as `title` of the product

- Prime User credentials

  ```text
   username: rahul
   password: rahul@2021
  ```

- Non-Prime User credentials

  ```text
   username: raja
   password: raja@2021
  ```
=======
- The banner image in the Team Matches Route should have the alt attribute value as `team banner`
- The alt attribute values for the images received from the response are given in the **Example response**
- The API responses received from the given api URLs should be converted to camel case
- Wrap the `Loader` component with an HTML container element and add the `testid` attribute value as `loader` to it as shown below
  ```
  <div testid="loader">
      <Loader type="Oval" color="#ffffff" height={50} width={50} />
  </div>
  ```
- Render HomeRoute component when path in URL matches `/`
- Render TeamMatchesRoute component when path in URL matches `/team-matches/:id`
- No need to use the `BrowserRouter` in `App.js` as we have already included in `index.js` file
- Each TeamMatchesRoute should have different gradient colors as background based on the selected team
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

### Resources

<details>
<<<<<<< HEAD
=======
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/ipl-dashboard-sm-bg.png](https://assets.ccbp.in/frontend/react-js/ipl-dashboard-sm-bg.png)
- [https://assets.ccbp.in/frontend/react-js/ipl-dashboard-lg-bg.png](https://assets.ccbp.in/frontend/react-js/ipl-dashboard-lg-bg.png)
- [https://assets.ccbp.in/frontend/react-js/ipl-logo-img.png](https://assets.ccbp.in/frontend/react-js/ipl-logo-img.png) alt should be **ipl logo**

</details>

<details>
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7
<summary>Colors</summary>

<br/>

<<<<<<< HEAD
<div style="background-color: #0b69ff; width: 150px; padding: 10px; color: white">Hex: #0b69ff</div>
<div style="background-color: #171f46; width: 150px; padding: 10px; color: white">Hex: #171f46</div>
<div style="background-color: #616e7c; width: 150px; padding: 10px; color: white">Hex: #616e7c</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
=======
**Background Colors**:

<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>
<div style="background-color: #a4261d; width: 150px; padding: 10px; color: white">Hex: #a4261d</div>
<div style="background-color: #5755a7; width: 150px; padding: 10px; color: white">Hex: #5755a7</div>
<div style="background-color: #d91c1f; width: 150px; padding: 10px; color: white">Hex: #d91c1f</div>
<div style="background-color: #f7db00; width: 150px; padding: 10px; color: white">Hex: #f7db00</div>
<div style="background-color: #ffffff33; width: 150px; padding: 10px; color: black">Hex: #ffffff33</div>
<div style="background-color: #da237b; width: 150px; padding: 10px; color: white">Hex: #da237b</div>
<div style="background-color: #13418b; width: 150px; padding: 10px; color: white">Hex: #13418b</div>
<div style="background-color: #f26d22; width: 150px; padding: 10px; color: white">Hex: #f26d22</div>
<div style="background-color: #4f5db0; width: 150px; padding: 10px; color: white">Hex: #4f5db0</div>
<div style="background-color: #0f172a; width: 150px; padding: 10px; color: white">Hex: #0f172a</div>
<br/>

**Border Colors**

<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #475569; width: 150px; padding: 10px; color: black">Hex: #475569</div>

<br />

**Text Colors**

<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #18ed66; width: 150px; padding: 10px; color: black">Hex: #18ed66</div>
<div style="background-color: #e31a1a; width: 150px; padding: 10px; color: black">Hex: #e31a1a</div>
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

<details>
<summary>Font-families</summary>

<<<<<<< HEAD
- Roboto
=======
- Bree Serif
>>>>>>> 855b91ca08eeb3d64178c2d60d05439047547ce7

</details>

> ### _Things to Keep in Mind_
>
> - All components you implement should go in the `src/components` directory.
> - Don't change the component folder names as those are the files being imported into the tests.
> - **Do not remove the pre-filled code**
> - Want to quickly review some of the concepts you’ve been learning? Take a look at the Cheat Sheets.
