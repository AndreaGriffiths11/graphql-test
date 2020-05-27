query {
  repositoryOwner(login: "andreagriffiths22") {
    repository(name: "graphql-test") {
      object(expression: "master") {
        ... on Commit {
          blame(path: "sting!") {
            ranges {
              startingLine
              endingLine
              age
              commit {
                oid
                author {
                  name
                }
              }
            }
          }
        }
      }
    }
  }
}
