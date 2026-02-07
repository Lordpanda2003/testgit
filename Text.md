### Partie 1: Document orienté model JSON


1. Faire un diagramme d'entité-relation des données suivante:

>```Course(code, title, description, credits, prerequisite) 

>Student(name, first_name, address)  

>Addresses(house_numbers, street, city, postal_code)```


Relations:
- Un élève peux suivre plusieurs cours
- Un cours es suivi par plusieurs élèves

![[student-cource-address.drawio(2).png]]


2. Fournir un exemple de structure JSON dans ce cas de figure

```json
{
  "_id": 1,
  "first_name": "Parfait",
  "last_name": "Moneze",
  "address": {
    "house_no": 45,
    "street": "Bruyère",
    "city": "Paris",
    "postal_code": "75010"
  },
  "courses": [
    {
      "code": "EM201",
      "title": "Data ",
      "description": "Introduction to DW concepts and NoSQL databases",
      "credits": 4,
      "prerequisites": [
        { "code": "API01", "title": "Introduction to Databases" }
      ]
    },
    {
      "code": "API10",
      "title": "Web Development",
      "description": "Frontend and backend web programming",
      "credits": 3
    }
  ]
}

```

