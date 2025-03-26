### API Documentation and Python Examples

#### Education and Learning APIs

##### 1. Open Library API
*Description: The Open Library API provides access to a vast collection of book information and metadata, allowing users to search for books and authors.*

**Documentation URL:** https://openlibrary.org/developers/api

**Endpoints and Parameters:**

*   **Search Books:** `/search.json`
    *   Parameters:
        *   `q`: Search term (required)

**Output:**  
The JSON output provides book information with these key fields:

- **numFound**: Total number of matching books
- **docs**: List of book entries containing:
    - **title**: Book title
    - **author_name**: Author(s) name
    - **first_publish_year**: First publication year
    - **edition_count**: Number of editions
    - **language**: Available language codes
    - **cover_i**: Cover image ID (use with `https://covers.openlibrary.org/b/id/{cover_i}-{size}.jpg`)
    - **key**: Unique book identifier
    - **author_key**: Author identifiers
    - **ia**: Internet Archive identifiers
    - **has_fulltext**: Full text availability status
    - **public_scan_b**: Public scan availability

##### 2. Open Trivia Database
*Description: The Open Trivia Database API provides access to a large database of trivia questions across various categories, suitable for building quiz applications.*

**Documentation URL:** https://opentdb.com/api_config.php

**Endpoints and Parameters:**

*   **Get Trivia Questions:** `/api.php`
    *   Parameters:
        *   `amount`: Number of questions (required, integer)

**Output:**  
The JSON output contains a list of trivia questions with these key fields:

- **response_code**: Status code (0 = success)
- **results**: List of question objects containing:
    - **category**: Question category
    - **type**: Question type ("multiple" or "boolean")
    - **difficulty**: Difficulty level ("easy", "medium", "hard")
    - **question**: The trivia question text
    - **correct_answer**: The correct answer
    - **incorrect_answers**: List of incorrect answers
##### 3. Numbers API
*Description: The Numbers API provides interesting facts about numbers, dates, and mathematical trivia, useful for educational applications or adding fun facts to projects.*

**Documentation URL:** http://numbersapi.com/ (homepage)

**Endpoints and Parameters:**

*   **Get Fact about a Number:** `/{number}`
    *   Number can be an integer or "random" for a random number.

###### Key Points:
- Output is plain text, not JSON
- No parsing required
- Direct use of `response.text`
- Simple error handling with status code check

##### 4. Cat Facts API
*Description: The Cat Facts API delivers random facts about cats, perfect for cat lovers or to add engaging content to applications.*

**Documentation URL:** https://alexwohlbruck.github.io/cat-facts/docs/

**Endpoints and Parameters:**

*   **Get a Cat Fact:** `/fact`
    *   No parameters needed for a random fact.
###### How to Use the Cat Fact Output

The JSON output provides a single cat fact. Let's examine its structure and how to use it:

###### JSON Structure 
The output is a JSON object (dictionary) with two key-value pairs:
- **fact**: Text of the cat fact (string)
- **length**: Length of the fact string (integer)

#### Entertainment and Social Engagement APIs

##### 5. Official Joke API
*Description: The Official Joke API provides random jokes in JSON format, ideal for adding humor to applications or creating joke-telling bots.*

**Documentation URL:** https://github.com/15Dkatz/official_joke_api

**Endpoints and Parameters:**

*   **Get Random Joke:** `/random_joke`
    *   No parameters needed for a random joke.
###### How to Use the Random Joke Output

The JSON output provides a random joke. Let's examine its structure and how to use it:

###### JSON Structure
The output is a JSON object (dictionary) with these key-value pairs:
- **type**: Joke category (e.g., "general")
- **setup**: First part of the joke (question/setup)
- **punchline**: Concluding part of the joke (answer/punchline)
- **id**: Unique joke identifier (integer)

##### 6. Rick and Morty API
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

###### How to Use the API Outputs

The API provides three main types of JSON outputs:

###### Character Output Structure
- **id**: Unique identifier (integer)
- **name**: Character name (string)
- **status**: Current status ("Alive", "Dead", "Unknown")
- **species**: Character species
- **type**: Character subspecies (if applicable)
- **gender**: Character gender
- **origin**: Object containing:
    - **name**: Origin location name
    - **url**: Location details URL
- **location**: Object containing current location info
- **image**: Character avatar URL
- **episode**: List of episode URLs
- **url**: Character API URL
- **created**: Creation timestamp

###### Location Output Structure
- **id**: Unique identifier (integer)
- **name**: Location name
- **type**: Location type
- **dimension**: Location dimension
- **residents**: List of character URLs
- **url**: Location API URL
- **created**: Creation timestamp

###### Episode Output Structure
- **id**: Unique identifier (integer)
- **name**: Episode title
- **air_date**: Original air date
- **episode**: Episode code
- **characters**: List of character URLs
- **url**: Episode API URL
- **created**: Creation timestamp
##### 7. Deck of Cards API
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
###### How to Use the Deck Draw Cards Output

The JSON output from drawing cards shows the result of a deck draw operation. Let's examine its structure:

###### JSON Structure
The output is a JSON object (dictionary) with these key-value pairs:
- **success**: Boolean indicating if draw request succeeded
- **deck_id**: Unique identifier of the deck (string)
- **cards**: List of drawn card objects, each containing:
    - **code**: Card code (e.g., "6H" for 6 of Hearts)
    - **image**: Card image URL (PNG)
    - **images**: Object with image format URLs:
        - **svg**: SVG image URL
        - **png**: PNG image URL
    - **value**: Card value (e.g., "6", "KING", "ACE")
    - **suit**: Card suit (HEARTS, DIAMONDS, SPADES, CLUBS)
- **remaining**: Number of cards left in deck (integer)
##### 8. Yes/No API
*Description: The Yes/No API provides a random "yes" or "no" answer, often with an animated GIF, a simple and fun API for decision-making applications or entertainment.*

**Documentation URL:** https://yesno.wtf/api (same page)

**Endpoints and Parameters:**

*   **Get Yes/No Answer:** `/api`
    *   No parameters needed for a random answer.
###### How to Use the Yes/No API Output

The JSON output provides a simple yes/no response. Let's examine its structure:

###### JSON Structure
The output is a JSON object (dictionary) with these key-value pairs:
- **answer**: Response ("yes" or "no")
- **forced**: Boolean indicating if response was forced
- **image**: GIF image URL matching the response
#### Productivity and Career Development APIs

##### 9. Agify.io
*Description: Agify.io predicts the age of a person based on their name, useful for demographic analysis or fun applications.*

**Documentation URL:** https://agify.io/documentation

**Endpoints and Parameters:**

*   **Predict Age by Name:** `/` (base URL)
    *   Parameters:
        *   `name`: Name to predict age for (required)

**How to Use the Agify.io API Output:**

This JSON output is the response from querying the Agify.io API to predict the age associated with a given name. Let's examine its structure and how to use it:

**JSON Structure:**

The output is a JSON object (dictionary) with the following key-value pairs:

- **count**: The number of times the name appears in the Agify.io dataset (integer). A higher count generally indicates a more reliable age prediction.
- **name**: The name that was queried (string). This confirms the name for which the age was predicted.
- **age**: The predicted age for the given name, based on the Agify.io data (integer).
##### 10. Nationalize.io
*Description: Nationalize.io predicts the nationality of a person based on their name, similar to Agify.io but for nationality prediction.*

**Documentation URL:** https://nationalize.io/documentation

**Endpoints and Parameters:**

*   **Predict Nationality by Name:** `/` (base URL)
    *   Parameters:
        *   `name`: Name to predict nationality for (required)
**How to Use the Nationalize.io API Output:**

This JSON output is the response from querying the Nationalize.io API to predict the nationality associated with a given name. Let's examine its structure and how to use it:

**JSON Structure:**

The output is a JSON object (dictionary) with the following key-value pairs:

- **count**: The number of times the name appears in the Nationalize.io dataset (integer). A higher count generally indicates a more reliable nationality prediction.
- **name**: The name that was queried (string). This confirms the name for which the nationality was predicted.
- **country**: A list of JSON objects, where each object represents a predicted country and its associated probability:
    - **country_id**: The two-letter ISO country code (e.g., "US" for United States, "GB" for United Kingdom) (string).
    - **probability**: The probability that the name is associated with that country (floating-point number between 0 and 1). A higher probability indicates a stronger association.
##### 11. Universities List API
*Description: The Universities List API provides access to a list of universities worldwide, searchable by country and name, great for educational applications or tools for students.*

**Documentation URL:** https://github.com/Hipo/university-domains-list-api

**Important Developer Notes:**

1. **Large Dataset Handling**: For countries with many universities (like United States, China, India), the API may return incomplete responses due to connection timeouts or large data transfers.

2. **Protocol Requirements**: Use HTTP instead of HTTPS for this API. The HTTPS version may not work reliably.

3. **Chunking Strategy**: When requesting data for large countries, implement a chunking strategy by querying universities alphabetically by first letter.

4. **Connection Management**:
   - Set longer timeouts (30-60 seconds) for larger countries
   - Implement retry mechanisms for connection failures
   - Add delays between requests to avoid overwhelming the API

5. **No Official Pagination**: The API lacks built-in pagination, requiring client-side implementation for limiting results.

6. **Error Handling**: Be prepared to catch and handle connection errors, including IncompleteRead exceptions.

7. **Filtering Options**:
   - Use the `country` parameter to filter by country name
   - Use the `name` parameter to further filter results by university name

8. **Response Format**: Returns a JSON array of universities with details like name, domains, web_pages, and country.

**Endpoints and Parameters:**

*   **Search Universities by Country:** `/search`
    *   Parameters:
        *   `country`: Country name (required)
        *   `name`: Filter by university name (optional)


### Output from running a Universities List API code snippet:

```json
[
    {
        "domains": [
            "uam.edu.ni"
        ],
        "name": "Universidad Americana",
        "alpha_two_code": "NI",
        "country": "Nicaragua",
        "state-province": null,
        "web_pages": [
            "http://www.uam.edu.ni/"
        ]
    },
    {
        "domains": [
            "ucyt.edu.ni"
        ],
        "name": "Universidad Nicarag\u00fcense de Ciencia y Tecnol\u00f3gica",
        "alpha_two_code": "NI",
        "country": "Nicaragua",
        "state-province": null,
        "web_pages": [
            "http://www.ucyt.edu.ni/"
        ]
    }
]
```
#### How to use the Universities List API output:

This JSON output is the response from querying a Universities List API for universities located in Nicaragua. It provides a list of university objects, each containing information about a specific university. Let's examine its structure and how to use it:

**JSON Structure:**

The output is a JSON array (list) of JSON objects. Each object represents a university and has the following key-value pairs:

- **domains**: A list of domain names associated with the university (list of strings).
- **name**: The name of the university (string).
- **alpha_two_code**: The two-letter ISO country code for the country where the university is located (string). In this case, it's "NI" for Nicaragua.
- **country**: The name of the country where the university is located (string).
- **state-province**: The state or province where the university is located (string or null if not applicable).
- **web_pages**: A list of web pages associated with the university (list of strings).


##### 12. Zippopotam API
*Description: The Zippopotam API retrieves information about ZIP codes and locations for various countries, useful for location-based applications or address verification.*

**Documentation URL:** http://www.zippopotam.us/

**Endpoints and Parameters:**

*   **Get ZIP Code Information:** `/{country_code}/{zip_code}`
    *   `country_code`: Two-letter country code (e.g., us, de)
    *   `zip_code`: ZIP code
    *   Example: `api.zippopotam.us/us/90210`

*   **Get Location Information:** `/{country_code}/{state}/{city}`
    *   `country_code`: Two-letter country code (e.g., us, de)
    *   `state`: State/province code or abbreviation
    *   `city`: City name
    *   Example: `api.zippopotam.us/us/ma/belmont`

**Output:**  
The JSON output provides location data with details like place names, postal codes, coordinates, and state information. The structure varies slightly depending on whether you're performing a ZIP code query or a location query.

###### How to Use the Zippopotam API Output

The Zippopotam API provides two types of JSON outputs depending on your query type:

1. **ZIP Code Query Output Structure:**
   - **post code**: The queried ZIP/postal code
   - **country**: Full country name
   - **country abbreviation**: Two-letter country code
   - **places**: List of locations associated with the ZIP code, each containing:
     - **place name**: Name of the location/city
     - **longitude**: Geographic longitude coordinate
     - **state**: Full state/province name
     - **state abbreviation**: Two-letter state/province code
     - **latitude**: Geographic latitude coordinate

2. **Location Query Output Structure:**
   - **country**: Full country name
   - **country abbreviation**: Two-letter country code
   - **state**: Full state/province name
   - **state abbreviation**: Two-letter state/province code
   - **place name**: Name of the queried location/city
   - **places**: List of postal codes and coordinates in that location, each containing:
     - **place name**: Name of the specific area
     - **post code**: ZIP/postal code for the area
     - **longitude**: Geographic longitude coordinate
     - **latitude**: Geographic latitude coordinate

This data can be useful for address verification, geocoding applications, or displaying location information on maps.

#### Mental Health and Wellness APIs

##### 13. Affirmations API
*Description: The Affirmations API provides positive affirmations to inspire and uplift, which can be used in wellness apps or daily motivation tools.*

**Documentation URL:** https://www.affirmations.dev/ (homepage)

**Endpoints and Parameters:**

*   **Get Affirmation:** `/` (base URL)
    *   No parameters needed for a random affirmation.

**Output:**  
The JSON output provides a single affirmation as a simple JSON object:

###### How to Use the Affirmations API Output

The JSON output from the Affirmations API is simple and straightforward:

###### JSON Structure
The output is a JSON object (dictionary) with one key-value pair:
- **affirmation**: The text of the positive affirmation (string)

This minimalist structure makes it very easy to extract and use the affirmation in your applications, whether for personal wellness tools, daily inspiration widgets, or motivational content.

#### Creative Tools APIs

##### 14. Art Institute of Chicago API
*Description: The Art Institute of Chicago API provides access to data about artworks from their collection, great for art-related applications or educational projects.*

**Documentation URL:** https://api.artic.edu/docs/

**Endpoints and Parameters:**

*   **Search Artworks:** `/api/v1/artworks/search`
    *   Parameters:
        *   `q`: Search query (e.g., cats, sunflowers)

**Output:**  
The JSON output provides detailed search results of artworks matching your query:

###### How to Use the Art Institute of Chicago API Output

The JSON response contains a comprehensive set of search results with metadata:

###### JSON Structure
- **pagination**: Object containing information about result pages:
  - **total**: Total number of matching artworks
  - **limit**: Number of results per page
  - **offset**: Starting position of results
  - **total_pages**: Total number of pages available
  - **current_page**: Current page number
- **data**: Array of artwork objects, each containing:
  - **_score**: Relevance score for the search
  - **id**: Unique artwork identifier
  - **api_model**: Type of object (usually "artworks")
  - **api_link**: Direct API link to full artwork details
  - **is_boosted**: Whether artwork was prioritized in results
  - **title**: Title of the artwork
  - **thumbnail**: Object containing image information:
    - **lqip**: Low-quality image placeholder (base64 encoded)
    - **width**: Original image width
    - **height**: Original image height
    - **alt_text**: Descriptive text for accessibility
  - **timestamp**: Date when the artwork data was last updated
- **info**: Copyright and licensing information
- **config**: Configuration URLs for IIIF image API and website

This data structure allows you to build rich art browsing applications, educational tools, or creative projects that leverage the museum's vast collection.

##### 15. DiceBear Avatars API
*Description: The DiceBear Avatars API generates customizable avatar images in various styles like pixel art, perfect for creating default avatars for users in applications.*

**Documentation URL:** https://www.dicebear.com/how-to-use/http-api/

**Endpoints and Parameters:**

*   **Generate Avatar:** `/{version}/{style}/svg`
    *   `version`: API version (e.g., 9.x)
    *   `style`: Avatar style (e.g., pixel-art, bottts, fun-emoji)
    *   **Key Parameters:**
        *   `seed`: Text string that determines which specific avatar is generated (same seed = same avatar)
        *   Various style-specific options (see style documentation)

**Note:** DiceBear generates SVG images that need to be saved to a file and displayed in a browser or embedded in HTML. Available avatar styles can be found at https://www.dicebear.com/styles/. Refer to the documentation for each style to get the correct style name to use in the API.

**Understanding Seeds:** The `seed` parameter is what makes each avatar unique and consistent. For example, if you use "john123" as the seed, it will always generate the same avatar design within a given style. This makes it perfect for user avatars - just use their username as the seed for a persistent avatar. Without a seed parameter, a random avatar is generated each time.

##### 16. Lorem Picsum API
*Description: The Lorem Picsum API provides placeholder images of various sizes and styles, essential for web development and design mockups.*

**Documentation URL:** https://picsum.photos/ (homepage)

**Endpoints and Parameters:**

*   **Get Placeholder Image:** `/{width}/{height}`
    *   `width`: Image width (integer)
    *   `height`: Image height (integer)


###### How to Use the Lorem Picsum API Output

The Lorem Picsum API returns a URL to a random placeholder image that matches your specified dimensions. Here's how to use the output:

###### URL Structure
The returned URL (e.g., `https://fastly.picsum.photos/id/966/400/200.jpg?hmac=sfUrBBEY6ZEQmNyqt-uhqNNrwElXvIAyhFs38wcetkE`) contains:
- Random image ID (`966` in this example)
- Your requested dimensions (`400/200`)
- A hash parameter for validation

###### Usage Options

1. you can open the link provided in a web browser
2. you can also use it in applications

##### 17. RoboHash API
*Description: The RoboHash API generates unique robot, monster, or alien images from text, fun for creating unique identifiers or avatars based on text input.*

**Documentation URL:** https://robohash.org/ (homepage)

**Endpoints and Parameters:**

*   **Generate Robot Image:** `/{text}.png`
    *   `text`: Text to generate robot from

**Output**
```html
https://robohash.org/beginner-api.png
```
This generates a url for a robot picture. You can open the url in a web browser or use it in an application


##### 18. JokeAPI
*Description: JokeAPI is a comprehensive API for jokes, offering various categories, languages, and filtering options, a more advanced joke API with extensive features.*

**Documentation URL:** https://jokeapi.dev/

**Endpoints and Parameters:**

*   **Get Joke:** `/joke/{categories}`
    *   `categories`: Joke categories (e.g., Programming, Christmas, Any, etc.)
    *   Parameters:
        *   `blacklistFlags`: Flags to blacklist (e.g., nsfw, racist, sexist, explicit, religious, political)
        *   `safe-mode`: Safe-mode flag (boolean)
        *   `format`: Response format (json, xml, yaml, txt)
        *   `lang`: Language code for jokes (en, es, de, fr, pt, cs)
        *   `type`: Type of joke to return (single, twopart)
        *   `contains`: Filter jokes containing specific string (case insensitive)
        *   `idRange`: Filter jokes by ID or ID range (e.g., 5-10, 42)
        *   `amount`: Number of jokes to return (max 10)

**Output:**  
The JokeAPI returns jokes in two possible formats:

###### JSON Structure for Two-Part Jokes
- **error**: Boolean indicating request success status (false = success)
- **category**: Joke category (e.g., "Programming")
- **type**: "twopart" for setup/punchline jokes
- **setup**: First part of the joke
- **delivery**: Punchline of the joke
- **flags**: Object with content warning flags (nsfw, religious, political, racist, sexist, explicit)
- **id**: Unique joke identifier
- **safe**: Whether joke matches safety parameters
- **lang**: Language code (e.g., "en")

###### JSON Structure for Single Jokes
Same as above, but with a single "joke" field instead of "setup" and "delivery" fields, and "type" will be "single".

The API's extensive filtering options make it suitable for applications requiring appropriate content control.