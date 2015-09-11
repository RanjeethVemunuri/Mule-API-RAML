/Movies:
   /{MovieTitle}
     get:
       queryParameters:
         author:
           displayName: Director
           type: string
           description: Directors Full Name
           example: Christopher Nolan
           required: false
         ReleaseYear:
           displayName: Release Year
           type: number
           description: The year released for the first time in the US
           example: 2014
           required: false
         rating:
           displayName: Rating
           type: number
           description: Average rating (1-5) submitted by users
           example: 3.14
           required: false
         imdb	:
           displayName: IMDB
           type: string
           minLength: 10
           example: 0321736079?
      put:
        queryParameters:
          access_token:
            displayName: Access Token
            type: string
            description: Token giving you permission to make call
            required: true
            
            //Responses
            
            /Movies:
   /{MovieTitles}:
     get:
       description: Retrieve a specific Movie title
       responses:
         200:
           body:
             application/json:
              example: |
                 {
                   "data": {
                     "id": "SbBGk",
                     "title": "Avengers: Age of Ultron",
                     "description": null,
                     "datetime": 1341533193,
                     "genre": "scienceFiction",
                     "author": "Mary Roach",
                     "link": "http://imdb.com/movies/2014",
                   },
                   "success": true,
                   "status": 200
                 }
