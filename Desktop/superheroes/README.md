# SuperHeroes

## Code Challenge

API backend project for tracking Heroes and their Powers.

## Technologies Used

- Ruby Version - ruby 2.7.4
- Ruby on Rails
- AMS - Active Model Serializer
- SQLite3

## Installation & Set up

Clone the repository

```
https://git@github.com:kericho/superheroes.git
```

Install Dependecies

```
bundle install
```

Migration and Seeding

```
rails db:migrate db:seed
```

Run Server

```
rails s
```

## Project Guidelines

#### Relationships

- A `Hero` has many `Powers` through `HeroPower`.
- A `Power` has many `Heros` through `HeroPower`.
- A `HeroPower` belongs to a `Hero` and belongs to a `Power`.

## Deliverables

GET /heroes

```
http://localhost:3000/heroes
```

```
[
    {
        "id": 1,
        "name": "Bruce Bunner",
        "super_name": "The Hulk"
    },
    {
        "id": 2,
        "name": "Jennifer Walters",
        "super_name": "She-Hulk"
    },
    {
        "id": 3,
        "name": "Thor Odinson",
        "super_name": "Thor-God of Thunder"
    },
    {
        "id": 4,
        "name": "Carol Danvers",
        "super_name": "Captain Marvel"
    },
    {
        "id": 5,
        "name": "Steve Rodgers",
        "super_name": "Captain America"
    },
    {
        "id": 6,
        "name": "Dr. Stephen Strange",
        "super_name": "Doctor Strange"
    },
    {
        "id": 7,
        "name": "Natasha Romanoff",
        "super_name": "Black Widow"
    }
]
```

GET /heroes/:id

```
http://localhost:3000/heroes/3
```

```
{
    "id": 3,
    "name": "Thor Odinson",
    "super_name": "Thor-God of Thunder",
    "powers": [
        {
            "id": 2,
            "name": "Manipulate Lightning",
            "description": "The ability to create and manipulate lightning."
        },
        {
            "id": 7,
            "name": "Super Reflex",
            "description": "The ability to react to situations with great speed."
        },
        {
            "id": 6,
            "name": "Super Smart",
            "description": "The ability to use your own intelligence to create gadgets that can be used to help in combat."
        },
        {
            "id": 5,
            "name": "Fighting",
            "description": "The ability to do combat without having extra-ability."
        }
    ]
}
```

GET /powers

```
http://localhost:3000/powers
```

```
[
    {
        "id": 1,
        "name": "Super Strong",
        "description": "The ability to have ability to lift, throw and stuff. Caused by gamma radiation overload."
    },
    {
        "id": 2,
        "name": "Manipulate Lightning",
        "description": "The ability to create and manipulate lightning."
    },
    {
        "id": 3,
        "name": "Flight",
        "description": "The ability to move through air by generating anti-gravitons thus negate the pull of gravity and fly, usually at incredibly fast speeds."
    },
    {
        "id": 4,
        "name": "Marksman",
        "description": "The ability to shoot arrows at incredible speeds to hit you target."
    },
    {
        "id": 5,
        "name": "Fighting",
        "description": "The ability to do combat without having extra-ability."
    },
    {
        "id": 6,
        "name": "Super Smart",
        "description": "The ability to use your own intelligence to create gadgets that can be used to help in combat."
    },
    {
        "id": 7,
        "name": "Super Reflex",
        "description": "The ability to react to situations with great speed."
    }
]
```

GET /powers/:id

```
{
    "id": 1,
    "name": "Super Strong",
    "description": "The ability to have ability to lift, throw and stuff. Caused by gamma radiation overload."
}
```

PATCH /powers/:id

- It accepts a JSON body with the following format: { "description": "Super Strength" }

POST /hero_powers

- It accepts a JSON body with the following format: { "strength": "Strong", "hero_id": 1, "power_id": 1 }
- Strength can be Strong, Weak, or Average

```
{
    "strength": "Strong",
    "hero_id": 1,
    "power_id": 1
}
```

## Bonus Deliverables

## Heroes

POST /heroes

- Creates a new Hero.

PATCH /heroes/:id

- Updates the heroes details.

DELETE /heroes/:id

- Deletes heroes from the Database.

## Powers

POST /powers

- Creates a new Power for heroes.

DELETE /powers/:id

- Deletes the PowerS from the Database.

## HeroPower

PATCH /hero_powers/:id

- Updates the HeroPower

DELETE /hero_powers/:id

- Deletes the HeroPower from the Database.

## Author Info

Elvis Rono
