# Bebeat Store

This repository was made for the [SvelteHack](https://hack.sveltesociety.dev/) event. Here we have a description of the project and later on when changes are pushed to the `main` branch. There will be a Demo Video Link and the link to the projects hosting url.

---

## Description
This project is called Bebeat store: its supposed to emulate a simple site like [Beatstars](https://www.beatstars.com) which is a platform that helps artists and producers sell their beats to other artists on the platform. This platform helps search for different types of beats according to artist, genre, or keywords. The platform later shows a list of beats according to the search criteria. Also other than selling beats, an artist can buy beats from other artists.

## Version History
- **Current: v0.0.0**
  - Front-End (Svelte):
    - Sign Up and Log In for artists
    - Search Filter for artist beats
    - Profile page of current logged in artist
    - Shopping Cart
    - Beat Upload
  - Back-End (Express + Mongo):
    - DB Model:
      - ```json
        "Artist" : {
            "docName": "Artist",
            "data": {
                "artistName": "String",
                "email": "String",
                "beats": ["Ref(Beat)"]
            }
        },
        "Beat" : {
            "docName": "Beat",
            "data": {
                "beatPlaylistName": "String",
                "songs": ["String"],
                "price": "Number",
                "url": "String" //Digital Ocean Spaces url (.zip file)
            }
        },
        "Order" : {
            "docName": "Order",
            "data": {
              "products": ["Ref(Beats)"],
              "totalPrice": "Number", //sum of products.price
              "createdAt": "Date"
            }
        }
        ```
        - Express Routing
        - Mongoose ORM
        - Mongo Atlas for DB Hosting
        - Digital Ocean Spaces for Storing beatPlaylistName.zip file
- **Future: V0.1.0**:
  - Back-End (Express + Mongo)
    - Compress Song Files programmatically