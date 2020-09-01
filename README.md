# GraphQL-Demo

Quick Start

Excute the commands below:

git clone https://github.com/IAshutoshMishra/GraphQL-Demo.git

cd GraphQL-Demo

npm i && npm start

Open the url http://localhost:4000/graphql, you will see the GraphiQL GUI in the window, and you can excute the example query and mution operations.
Query Operation

Request

query {

  user(id: 1) {
  
    name
    
    nickname
    
    message {
    
      id
      
      content
      
    }
    
  }
  
}

Response

{
  "data": {
  
    "user": [
    
      {
      
        "name": "gin",
        
        "nickname": "lancegin",
        
        "message": [
        
          {
          
            "id": "1",
            
            "content": "test message"
            
          },
          
          {
          
            "id": "2",
            
            "content": "hello"
            
          },
          
          {
          
            "id": "3",
            
            "content": "world"
            
          }
          
        ]
        
      }
      
    ]
    
  }
  
}

Mutation Operation
Request

mutation {

  createMessage(input: {user_id: "1", content: "hello world111"}) {
  
    id
    
    content
    
  }
  
}

Response

{
  "data": {
  
    "createMessage": {
    
      "id": "10",
      
      "content": "hello world111"
      
    }
    
  }
  
}
