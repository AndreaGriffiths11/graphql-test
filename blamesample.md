query {
  repositoryOwner(login: "andreagriffiths22") {
    repository(name: "graphql-test") {
      object(expression: "master") {
        ... on Commit {
          blame(path: "string!") {
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
