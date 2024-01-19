#### Register user
```
curl -X POST -H "Content-Type: application/json" -d '{"username": "new_user", "password": "new_password"}' http://127.0.0.1:8000/api/register/ 
```

#### Obtain Authentication Token:
```
curl -X POST -H "Content-Type: application/json" -d '{"username": "new_user", "password": "new_password"}' http://127.0.0.1:8000/api/login/
```

#### Get the list of students:
```
curl -H "Authorization: Token your_token" http://127.0.0.1:8000/api/students/
```
#### Create a new student:
```
curl -X POST -H "Content-Type: application/json" -H "Authorization: Token your_token" -d '{"name": "John Doe", "marks": 85.5}' http://127.0.0.1:8000/api/students/
```
#### Get details of a specific student (replace {id} with the actual student ID):
```
curl -H "Authorization: Token your_token" http://127.0.0.1:8000/api/students/{id}/
```
#### Update a student (replace {id} with the actual student ID):
```
curl -X PUT -H "Content-Type: application/json" -H "Authorization: Token your_token" -d '{"name": "Updated Name", "marks": 90.0}' http://127.0.0.1:8000/api/students/{id}/
```

#### Delete a student (replace {id} with the actual student ID):
```
curl -X DELETE -H "Authorization: Token your_token" http://127.0.0.1:8000/api/students/{id}/
```
