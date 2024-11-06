# Sneaker DB StockX - Light Version

## Introduction

**Sneaker DB StockX - Light Version API** allows you to get every sneaker-related information you need including images, product links as well as prices from StockX. The data is from StockX, the sneaker shopping platform.

## Authentication

The URL you need to use is the following: `https://sneaker-db-stockx-light-version.p.rapidapi.com/`
The API requires the headers listed below:

- **`x-rapidapi-host`**: `sneaker-db-stockx-light-version.p.rapidapi.com`
- **`x-rapidapi-key`**: `YOUR_API_KEY`

Make sure to replace `YOUR_API_KEY` with your API key. You can register one [here](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/sneaker-db-stockx-light-version/pricing).
Some frameworks automatically add extra headers, you have to make sure to remove them in order to get a response from the API.

## Endpoints

The API is configured to accept only **GET** requests. Below are the available endpoints with their descriptions and required parameters.

### 1. **`GET /relatedProducts`**

- **Description**: Retrieves related products of each product.

| Parameter | Type   | Default | Description                                 | Required |
|-----------|--------|---------|---------------------------------------------|----------|
| `urlKey`  | string | -       | The name of the product                     | Yes      |

Example request:

```javascript
fetch('https://sneaker-db-stockx-light-version.p.rapidapi.com/relatedProducts?urlKey=air-jordan-1-high-zoom-air-cmft-2-honeydew', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'sneaker-db-stockx-light-version.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "adIdentifier": null,
    "adInventoryType": "STANDARD",
    "node": {
      "id": "8cfcea95-370a-4e7f-8d06-88199b09a3da",
      "favorite": null,
      "urlKey": "air-jordan-1-high-zoom-air-cmft-2-dark-powder-blue",
      "productCategory": "sneakers",
      "primaryCategory": "Air Jordan",
      "brand": "Jordan",
      "name": "Dark Powder Blue",
      "model": "Jordan 1 High Zoom Air CMFT 2",
      "listingType": "STANDARD",
      "lockBuying": false,
      "lockSelling": false,
      "title": "Jordan 1 High Zoom Air CMFT 2 Dark Powder Blue",
      "gender": "men",
      "browseVerticals": [
        "sneakers"
      ],
      "market": {
        "state": {
          "numberOfCustodialAsks": 14,
          "lowestCustodialAsk": {
            "amount": 93
          },
          "lowestAsk": {
            "amount": 80
          },
          ...
```

### 2. **`GET /productsDetail`**

- **Description**: Retrieves product full details, such as description, price, last sale and much more.

| Parameter | Type   | Default | Description                                 | Required |
|-----------|--------|---------|---------------------------------------------|----------|
| `urlKey`  | string | -       | The name of the product                     | Yes      |

Example request:

```javascript
fetch('https://sneaker-db-stockx-light-version.p.rapidapi.com/productsDetail?urlKey=air-jordan-1-high-zoom-air-cmft-2-honeydew', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'sneaker-db-stockx-light-version.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "product": {
    "id": "f74c8a47-55cd-4784-8c04-3a7496e92701",
    "uuid": "f74c8a47-55cd-4784-8c04-3a7496e92701",
    "name": "Jordan 1 High Zoom Air CMFT 2 Honeydew",
    "brand": "Jordan",
    "thumbnail_url": "https://images.stockx.com/images/Air-Jordan-1-High-Zoom-Air-CMFT-2-Honeydew-Product.jpg?fit=fill&bg=FFFFFF&w=300&h=214&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1705599062",
    "media": {
      "imageUrl": "https://images.stockx.com/images/Air-Jordan-1-High-Zoom-Air-CMFT-2-Honeydew-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1705599062",
      "smallImageUrl": "https://images.stockx.com/images/Air-Jordan-1-High-Zoom-Air-CMFT-2-Honeydew-Product.jpg?fit=fill&bg=FFFFFF&w=300&h=214&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1705599062",
      "thumbUrl": "https://images.stockx.com/images/Air-Jordan-1-High-Zoom-Air-CMFT-2-Honeydew-Product.jpg?fit=fill&bg=FFFFFF&w=140&h=100&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1705599062",
      "gallery": [],
      "hidden": false
    },
    "url": "air-jordan-1-high-zoom-air-cmft-2-honeydew",
    "release_date": "",
    "categories": [
      "Air Jordan",
      "One"
    ],
    "categoryPath": {
      "L1": [
        "sneakers"
      ],
      "L2": [
        "sneakers > lifestyle"
      ],
      "L3": null,
      "Max": [
        "sneakers > lifestyle"
        ...
```

### 3. **`GET /searchv1`**

- **Description**: Retrieves data from any search query.

| Parameter | Type   | Default | Description                                 | Required |
|-----------|--------|---------|---------------------------------------------|----------|
| `s`       | string | -       | The name to search for                      | Yes      |
| `perPage` | string | -       | The number of results per page              | No       |

Example request:

```javascript
fetch('https://sneaker-db-stockx-light-version.p.rapidapi.com/searchv1?s=yeezy', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'sneaker-db-stockx-light-version.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "shoeName": "adidas Yeezy Slide Slate Marine",
    "brand": "adidas",
    "silhoutte": "adidas Yeezy Slide",
    "styleID": "ID2349",
    "make": "adidas Yeezy Slide",
    "colorway": "Slate Marine/Slate Marine/Slate Marine",
    "retailPrice": 70,
    "thumbnail": "https://images.stockx.com/images/adidas-Yeezy-Slide-Slate-Marine-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1691071483",
    "releaseDate": "2024-05-27",
    "description": "The adidas Yeezy Slide in Slate Marine showcases an unprecedented combination of style and comfort. The slate marine colorway released on August 11, 2023 ...",
    "resellLinks": {
      "stockX": "https://stockx.com/adidas-yeezy-slide-slate-marine"
    },
    "lowestResellPrice": {
      "stockX": 77
    }
  },
  {
    "shoeName": "adidas Yeezy Slide Onyx",
    "brand": "adidas",
    "silhoutte": "adidas Yeezy Slide",
    "styleID": "HQ6448",
    "make": "adidas Yeezy Slide",
    "colorway": "Onyx/Onyx/Onyx",
    "retailPrice": 60,
    "thumbnail": "https://images.stockx.com/images/adidas-Yeezy-Slide-Black-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1646687426",
    "releaseDate": "2024-05-27",
```

### 4. **`GET /searchv2`**

- **Description**: Retrieves data from any search query.

| Parameter | Type   | Default | Description                                 | Required |
|-----------|--------|---------|---------------------------------------------|----------|
| `query`   | string | -       | The name to search for                      | Yes      |
| `perPage` | number | `0`     | The number of results per page              | No       |
| `page`    | number | -       | The page number to search results           | No       |

Example request:

```javascript
fetch('https://sneaker-db-stockx-light-version.p.rapidapi.com/searchv2?query=yeezy', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'sneaker-db-stockx-light-version.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
{
  "products": {
    "edges": [
      {
        "objectId": "045ae5b2-b79e-47c2-8f71-f82ab57df7a5",
        "isAd": false,
        "adId": null,
        "adInventoryType": null,
        "node": {
          "id": "045ae5b2-b79e-47c2-8f71-f82ab57df7a5",
          "name": "Onyx",
          "urlKey": "adidas-yeezy-foam-rnnr-onyx",
          "title": "adidas Yeezy Foam RNR Onyx",
          "brand": "adidas",
          "description": "The adidas Yeezy Foam RNR Onyx arrives with an Onyx, oval-cut foam construction made of part EVA and algae. At the base, a cushioned footbed offers comfort and support, while a sculptural sole with deep treads provides traction.\n<br>\n<br>\nThe adidas Yeezy Foam RNR Onyx released in June of 2022 and retailed for $80 and in March of 2024 and retailed for $90.",
          "model": "adidas Yeezy Foam RNR",
          "condition": "New",
          "productCategory": "sneakers",
          "listingType": "STANDARD",
          "gender": "men",
          "browseVerticals": [
            "sneakers"
          ],
          "media": {
            "thumbUrl": "https://images.stockx.com/images/adidas-Yeezy-Foam-RNNR-Onyx-Product.jpg?fit=fill&bg=FFFFFF&w=140&h=100&fm=webp&auto=compress&q=90&dpr=2&trim=color&updated_at=1654264132",
            "smallImageUrl": "https://images.stockx.com/images/adidas-Yeezy-Foam-RNNR-Onyx-Product.jpg?fit=fill&bg=FFFFFF&w=300&h=214&fm=webp&auto=compress&q=90&dpr=2&trim=color&updated_at=1654264132"
          },
          "favorite": null,
          "productTraits": [
            {
              ...
```

### 5. **`GET /searchv3`**

- **Description**: Retrieves data from any search query.

| Parameter | Type   | Default | Description                                 | Required |
|-----------|--------|---------|---------------------------------------------|----------|
| `s`       | string | -       | The name to search for                      | Yes      |

Example request:

```javascript
fetch('https://sneaker-db-stockx-light-version.p.rapidapi.com/searchv3?s=yeezy', {
  method: 'GET',
  headers: {
    'x-rapidapi-host': 'sneaker-db-stockx-light-version.p.rapidapi.com',
    'x-rapidapi-key': 'API_KEY' // Replace 'API_KEY' with your API key
  }
})
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

Example response:

```json
[
  {
    "name": "adidas Yeezy Slide Slate Marine",
    "pid": "ID2349",
    "image": "https://images.stockx.com/images/adidas-Yeezy-Slide-Slate-Marine-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1691071483",
    "uuid": "516b48dd-cd5b-4660-bfc1-4dcd9c387a66",
    "searchKey": "adidas-Yeezy-Slide-Slate-Marine",
    "details": {
      "retail": 70,
      "releaseDate": "2024-05-27",
      "colorway": "Slate Marine/Slate Marine/Slate Marine",
      "brand": "adidas",
      "type": "adidas Yeezy Slide",
      "gender": "men",
      "description": "The adidas Yeezy Slide in Slate Marine showcases an unprecedented combination of style and comfort. The slate marine colorway released on August 11, 2023..."
    }
  },
  {
    "name": "adidas Yeezy Slide Onyx",
    "pid": "HQ6448",
    "image": "https://images.stockx.com/images/adidas-Yeezy-Slide-Black-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&trim=color&q=90&dpr=2&updated_at=1646687426",
    "uuid": "ccc77727-c82d-48f8-8c61-9eb5b183a950",
    "searchKey": "adidas-Yeezy-Slide-Black",
    "details": {
      "retail": 60,
      "releaseDate": "2024-05-27",
      "colorway": "Onyx/Onyx/Onyx",
      "brand": "adidas",
      "type": "adidas Yeezy Slide",
      "gender": "men",
      ...
```

## Error Handling

The  API returns standard HTTP status codes to indicate the success or failure of API requests. Below are common errors and suggestions for handling them.

|Status Code|Message|Description|Suggested Handling|
|--|--|--|--|
| **400** | Bad Request | The request was malformed or missing required parameters (e.g., `domain` parameter not provided). | Verify that all required parameters are included and correctly formatted. |
| **401** | Unauthorized | Invalid or missing API key in the request headers. | Check that a valid API key is included in `x-rapidapi-key`. |
| **403** | Forbidden | Access to the requested resource is denied, possibly due to rate limits or restricted access. | Review rate limits and ensure API permissions. Retry after a delay if rate limit exceeded. |
| **404** | Not Found | The requested domain information could not be found (e.g., domain does not exist). | Check the spelling or availability of the domain. |
| **429** | Too Many Requests | The API rate limit has been exceeded. | Implement rate-limiting logic and retry after the specified rate limit reset time. |
| **500** | Internal Server Error | A server error occurred while processing the request. | Retry the request after a few seconds. If the error persists, contact API support. |
| **503** | Service Unavailable | The API service is temporarily unavailable (e.g., due to maintenance). | Retry the request later or check the API status page for maintenance alerts. |
