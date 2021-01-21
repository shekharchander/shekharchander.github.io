# A quick guide to Youtube Search APi available on : https://rapidapi.com/shekhar1000.sc/api/youtube-advanced-search/
### Basics
The Api takes following parameters : 
1. query #The search query
2. count #Number of results you want. (The bigger the number, more time it takes)
3. filters #Filters you want to apply. (Filters documentation can be found [here](#filter-documentation)

### Usage
A Quick Example of how to use the API:

url = "https://youtube-advanced-search.p.rapidapi.com/search"

querystring = {
    "query":"hello", # Defines the search word
    "count":"1", # Defines count of Search results
    "filters":"udlh" # Filters to apply on results
    }

headers = {
    'x-rapidapi-key': "Your API Key",
    'x-rapidapi-host': "youtube-advanced-search.p.rapidapi.com"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)


### Filter Documentation

| Filter                         | filter name |
|--------------------------------|-------------|
| Upload Date : Last Hour        | udlh        |
| Upload Date : Today            | udtd        |
| Upload Date : This Week        | udtw        |
| Upload Date : This Month       | udtm        |
| Upload Date : This Year        | udty        |
| Type : Video                   | tyvi        |
| Type : Channel                 | tych        |
| Type : Playlist                | typl        |
| Type : Film                    | tyfi        |
| Type : Programme               | typr        |
| Duration : Short (< 4 Minutes) | dush        |
| Duration : Long (> 20 Minutes) | dulo        |
| Features : Live                | feli        |
| Features : 4K                  | fe4k        |
| Features : HD                  | fehd        |
| Features : Subtitles/CC        | fesu        |
| Features : Creative Commons    | fecc        |
| Features : 360                 | fe36        |
| Features : VR180               | fevr        |
| Features : 3D                  | fe3d        |
| Features : HDR                 | fehd        |
| Features : Location            | felo        |
| Features : Purchased           | fepu        |
| Sort By : Relevance            | sore        |
| Sort By : Upload date          | soup        |
| Sort By : View Count           | sovi        |
| Sort By : Rating               | sora        |
