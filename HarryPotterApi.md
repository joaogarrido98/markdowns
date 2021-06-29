# The Magical Harry Potter API

## This is an API for people who love Harry Potter and Coding

![Homepage](./harry/screenshot.JPG)

This project was made with the intention of learning how to create RESTApi's and it's based on the characters created by J.K.Rowling.

# Usage

This is a step by step of how to use the API

The api consists of a number of endpoints that are fetched through any language.

Javascript will be used to show examples on how to use the API.

## Endpoints

**All endpoints have the following pre url : TO BE INPUTED**

**All ID endpoints have the same response but on a specific ID**

<table>
<tr>
<td> <b><code>GET</code></b> </td> <td> <b>Response - JSON</b> </td>
</tr>
<tr>
<td> /character </td>
<td>
<pre>
<code>
{
  "id": 1,
  "actor": "Daniel Radcliffe",
  "alive": true,
  "ancestry": "half-blood",
  "dateOfBirth": {
    "year": 1980,
    "month": 7,
    "day": 31
  },
  "gender": "male",
  "hogwartsOccupation": "student",
  "house": "Gryffindor",
  "image": "",
  "patronus": "stag",
  "species": "human",
  "name": "Harry Potter"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /character/{id} </td>
<td>
    Same response as above
</td>
</tr>
<tr>
<td> /patronus </td>
<td>

<pre>
<code>
{
  "patronus_id": 2,
  "patronus_title": "stag"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /patronus/{id} </td>
<td>
    Same response as above
</td>
</tr>
<tr>
<td> /spells </td>
<td>
<pre>
<code>
{
  "spell_id": 2,
  "spell_title": "accio"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /spells/{id} </td>
<td>
    Same response as above
</td>
</tr>
<tr>
<td> /species </td>
<td>
<pre>
<code>
{
  "species_id": 2,
  "species_title": "werewolf"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /species/{id} </td>
<td>
    Same response as above
</td>
</tr>
<tr>
<td> /houses </td>
<td>
<pre>
<code>
{
  "house_id": 4,
  "house_title": "Slytherin"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /houses/{id} </td>
<td>
    Same response as above
</td>
</tr>
<tr>
<td> /ancestries </td>
<td>
<pre>
<code>
{
  "ancestry_id": 3,
  "ancestry_title": "half-blood"
}
</code>
</pre>
</td>
</tr>
<tr>
<td> /ancestries/{id} </td>
<td>
    Same response as above
</td>
</tr>
</table>

### Error Responses

- **Code: 404** Not Found

  Content: No request with that id found

  Found when id requested doesn't exist in database.

- **Code: 401** Bad Request

  Content: Id parameter has to be a number

  Found when id requested isn't in the correct format.

## Samples

All samples will be showed using the character endpoints

### Get All Character

```javascript
document.addEventListener("DOMContentLoaded", () => {
  fetch("url/characters")
    .then((response) => response.json())
    .then((data) => {
      console.log(data);
    });
});
```

### Get Specific Character

```javascript
document.addEventListener("DOMContentLoaded", () => {
  fetch("url/characters/1")
    .then((response) => response.json())
    .then((data) => {
      console.log(data);
    });
});
```

# Copyright

The Magical Harry Potter Api is a non-commercial project.

## Content

Harry Potter and all associated names are copyright J.K. Rowling and Warner Bros.
