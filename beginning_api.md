### API Documentation and Python Examples

#### Education and Learning APIs

##### 1. Open Library API
*Description: The Open Library API provides access to a vast collection of book information and metadata, allowing users to search for books and authors.*

**Documentation URL:** https://openlibrary.org/developers/api

**Endpoints and Parameters:**

*   **Search Books:** `/search.json`
    *   Parameters:
        *   `q`: Search term (required)

##### 2. Open Trivia Database
*Description: The Open Trivia Database API provides access to a large database of trivia questions across various categories, suitable for building quiz applications.*

**Documentation URL:** https://opentdb.com/api_config.php

**Endpoints and Parameters:**

*   **Get Trivia Questions:** `/api.php`
    *   Parameters:
        *   `amount`: Number of questions (required, integer)

##### 3. Numbers API
*Description: The Numbers API provides interesting facts about numbers, dates, and mathematical trivia, useful for educational applications or adding fun facts to projects.*

**Documentation URL:** http://numbersapi.com/ (homepage)

**Endpoints and Parameters:**

*   **Get Fact about a Number:** `/{number}`
    *   Number can be an integer or "random" for a random number.

##### 4. Cat Facts API
*Description: The Cat Facts API delivers random facts about cats, perfect for cat lovers or to add engaging content to applications.*

**Documentation URL:** https://alexwohlbruck.github.io/cat-facts/docs/

**Endpoints and Parameters:**

*   **Get a Cat Fact:** `/fact`
    *   No parameters needed for a random fact.

#### Entertainment and Social Engagement APIs

##### 5. Official Joke API
*Description: The Official Joke API provides random jokes in JSON format, ideal for adding humor to applications or creating joke-telling bots.*

**Documentation URL:** https://github.com/15Dkatz/official_joke_api

**Endpoints and Parameters:**

*   **Get Random Joke:** `/random_joke`
    *   No parameters needed for a random joke.

##### 6. Shibe.Online API
*Description: The Shibe.Online API provides random images of Shiba Inu dogs, cats, and birds, perfect for adding visual appeal to applications or creating fun image displays.*

**Documentation URL:** https://shibe.online/

**Endpoints and Parameters:**

*   **Get Shibe Images:** `/api/shibes`
*   **Get Cat Images:** `/api/cats`
*   **Get Bird Images:** `/api/birds`
    *   Parameters (for all endpoints):
        *   `count`: Number of images (integer)

##### 7. Rick and Morty API
*Description: The Rick and Morty API provides access to character, location, and episode data from the animated show Rick and Morty, ideal for fan projects or applications related to the show.*

**Documentation URL:** https://rickandmortyapi.com/documentation/

**Endpoints and Parameters:**

*   **Get Character by ID:** `/character/{id}`
    *   `id`: Character ID (integer)
*   **Get All Characters:** `/character`
*   **Get Location by ID:** `/location/{id}`
*   **Get All Locations:** `/location`
*   **Get Episode by ID:** `/episode/{id}`
*   **Get All Episodes:** `/episode`

##### 8. Deck of Cards API
*Description: The Deck of Cards API simulates actions with a deck of cards, such as shuffling and drawing cards, useful for building card games or applications requiring card dealing logic.*

**Documentation URL:** https://www.deckofcardsapi.com/

**Endpoints and Parameters:**

*   **Shuffle New Deck:** `/api/deck/new/shuffle/`
    *   Parameters:
        *   `deck_count`: Number of decks (integer)
*   **Draw Card(s):** `/api/deck/{deck_id}/draw/`
    *   Parameters:
        *   `count`: Number of cards to draw (integer)
*   **Shuffle Existing Deck:** `/api/deck/{deck_id}/shuffle/`
*   **Add to Pile:** `/api/deck/{deck_id}/pile/{pile_name}/add/`
    *   Parameters:
        *   `cards`: Comma-separated card codes

##### 9. Yes/No API
*Description: The Yes/No API provides a random "yes" or "no" answer, often with an animated GIF, a simple and fun API for decision-making applications or entertainment.*

**Documentation URL:** https://yesno.wtf/api (same page)

**Endpoints and Parameters:**

*   **Get Yes/No Answer:** `/api`
    *   No parameters needed for a random answer.

#### Productivity and Career Development APIs

##### 10. Agify.io
*Description: Agify.io predicts the age of a person based on their name, useful for demographic analysis or fun applications.*

**Documentation URL:** https://agify.io/documentation

**Endpoints and Parameters:**

*   **Predict Age by Name:** `/` (base URL)
    *   Parameters:
        *   `name`: Name to predict age for (required)

##### 11. Nationalize.io
*Description: Nationalize.io predicts the nationality of a person based on their name, similar to Agify.io but for nationality prediction.*

**Documentation URL:** https://nationalize.io/documentation

**Endpoints and Parameters:**

*   **Predict Nationality by Name:** `/` (base URL)
    *   Parameters:
        *   `name`: Name to predict nationality for (required)

##### 12. Universities List API
*Description: The Universities List API provides access to a list of universities worldwide, searchable by country and name, great for educational applications or tools for students.*

**Documentation URL:** https://github.com/Hipo/university-domains-list-api

**Endpoints and Parameters:**

*   **Search Universities by Country:** `/search`
    *   Parameters:
        *   `country`: Country name (required)

##### 13. Data USA API
*Description: The Data USA API provides public data about the United States, including demographics and economy, useful for data analysis projects or applications requiring US public data.*

**Documentation URL:** https://datausa.io/about/api/

**Endpoints and Parameters:**

*   **Get Data:** `/api/data`
    *   Parameters:
        *   `drilldowns`: Data categories to drill down into (e.g., Nation, State, Year)
        *   `measures`: Measures to retrieve (e.g., Population, GDP)

##### 14. Zippopotam API
*Description: The Zippopotam API retrieves information about ZIP codes for various countries, useful for location-based applications or address verification.*

**Documentation URL:** http://www.zippopotam.us/

**Endpoints and Parameters:**

*   **Get ZIP Code Information:** `/{country_code}/{zip_code}`
    *   `country_code`: Two-letter country code (e.g., us, de)
    *   `zip_code`: ZIP code

#### Mental Health and Wellness APIs

##### 15. Affirmations API
*Description: The Affirmations API provides positive affirmations to inspire and uplift, which can be used in wellness apps or daily motivation tools.*

**Documentation URL:** https://www.affirmations.dev/ (homepage)

**Endpoints and Parameters:**

*   **Get Affirmation:** `/` (base URL)
    *   No parameters needed for a random affirmation.

#### Creative Tools APIs

##### 17. Art Institute of Chicago API
*Description: The Art Institute of Chicago API provides access to data about artworks from their collection, great for art-related applications or educational projects.*

**Documentation URL:** https://api.artic.edu/docs/

**Endpoints and Parameters:**

*   **Search Artworks:** `/api/v1/artworks/search`
    *   Parameters:
        *   `q`: Search query (e.g., cats, sunflowers)

##### 18. COLOURlovers API
*Description: The COLOURlovers API allows exploration of color palettes, patterns, and color-related data, useful for design applications or projects involving color schemes.*

**Documentation URL:** https://www.colourlovers.com/api/

**Endpoints and Parameters:**

*   **Get New Colors:** `/api/colors/new`
    *   Parameters:
        *   `format`: Response format (e.g., json, xml, api)

##### 19. DiceBear Avatars API
*Description: The DiceBear Avatars API generates customizable avatar images in various styles like pixel art, perfect for creating default avatars for users in applications.*

**Documentation URL:** https://www.dicebear.com/how-to-use/http-api/

**Endpoints and Parameters:**

*   **Generate Avatar:** `/{version}/{style}/svg`
    *   `version`: API version (e.g., 9.x)
    *   `style`: Avatar style (e.g., pixel-art, bottts, fun-emoji)

##### 20. Lorem Picsum API
*Description: The Lorem Picsum API provides placeholder images of various sizes and styles, essential for web development and design mockups.*

**Documentation URL:** https://picsum.photos/ (homepage)

**Endpoints and Parameters:**

*   **Get Placeholder Image:** `/{width}/{height}`
    *   `width`: Image width (integer)
    *   `height`: Image height (integer)

##### 21. RoboHash API
*Description: The RoboHash API generates unique robot, monster, or alien images from text, fun for creating unique identifiers or avatars based on text input.*

**Documentation URL:** https://robohash.org/ (homepage)

**Endpoints and Parameters:**

*   **Generate Robot Image:** `/{text}.png`
    *   `text`: Text to generate robot from

##### 22. JokeAPI
*Description: JokeAPI is a comprehensive API for jokes, offering various categories, languages, and filtering options, a more advanced joke API with extensive features.*

**Documentation URL:** https://jokeapi.dev/

**Endpoints and Parameters:**

*   **Get Joke:** `/joke/{categories}`
    *   `categories`: Joke categories (e.g., Programming, Christmas, Any, etc.)
    *   Parameters:
        *   `blacklistFlags`: Flags to blacklist (e.g., nsfw, racist, sexist)
        *   `safe-mode`: Safe-mode flag (boolean)