# Hackofiesta

Link of the project: https://tanishabisht.github.io/CaffeineOverflow-FrontEnd

## HOW TO INSTALL
You must have the following tools installed in your PC
1. Node Packange Manager
2. COde Editor (preferred VSC)

Guidelines to run the project
1. Pull the repo in your local
2. In your command line, write the code `npm install` to install all the dependancies
3. To run in your local machine, write the code `npm start`

Run the backend in Linux/macOS, as we need turicreate that run in Linux/macOS only

## Database

The JSON object that will be extracted from the database:

1. For listing all projects 
   - **GET : /fetchAll**
```
const dbVals = [
    {
        id: <unique id>,
        projName: <Name of the project>,
        projDesc: <mini description of the project>,
        stacks: <Array of stacks> ['NODE JS', 'MongoDB', 'ReactJS'],
        projLinks: <Array of links> ['#', '#'],
        inDesc: <Detail description of the project>,
        category: <dynamically generated by our ML model>
    }
]
```



2. For searching projects based on Names
   - **GET : /fetchbyName/{projName}**



3. For listing all the project Names
   - **GET : /fetchAllProjName**
```
[
    'ALL',
    'DONTRACK',
    'AnonyMate',
    'Peer IO',
    'MediFast',
    'Ularn'
]
```



4. Fetch By ML generated tags
   - **GET : /fetchHealth**
   - **GET : /fetchEducation**
   - **GET : /fetchMentalhealth**
   - **GET : /fetchSafety**
   - **GET : /fetchMisc**
   - **GET : /fetchTech**
   - **GET : /fetchScience**
   - **GET : /fetchGeneral**



5. Fetch Projects that are given special mentions
   - **GET : /fetchSpecialMention**





6. For Searching projects based on the filters created by ML model
   - **GET : /fetchLabelAndURL**
```
[
    {label: 'safety and wellbeing', fetchUrl: 'fetchSafety'},
    {label: 'mental health', fetchUrl: 'fetchSafety'},
    {label: 'miscellaneous', fetchUrl: 'fetchMisc'},
    {label: 'health and wellness', fetchUrl: 'fetchSafety'},
    {label: 'general wellfare', fetchUrl: 'fetchSafety'},
    {label: 'technology', fetchUrl: 'fetchTech'},
    {label: 'education', fetchUrl: 'fetchSafety'},
    {label: 'science and research', fetchUrl: 'fetchScience'},
    {label: 'special mention', fetchUrl: 'fetchSpecialMention'}
]
```



7. For listing all the Stacks
   - **GET : /FecthAllStacks**
```
[
    "Solidity",
    "Infura",
    "Nodejs",
    "discord.js",
    "Superfluid"
]
```



8. Fetch Projects By Stacks
   - **GET : /FecthByStacks/{stackName}**



9. For Comment Section
```
const chatVals = [
    {
        id: <unique id>
        projId: <project ID the chats belong to>, 
        username: <username of the user>', 
        chat: <message sent by the user>
    }
]
```