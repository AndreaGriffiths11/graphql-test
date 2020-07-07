query SearchMostTop10Star($queryString: String!, $numberRepos:Int!) {
  search(query: $queryString, type: REPOSITORY, first: $numberRepos) {
    repositoryCount
    edges {
      node {
        ... on Repository {
          name
          url
          description
#         shortDescriptionHTML
          createdAt
          pushedAt
          updatedAt
          releases {releases: totalCount}
          forks: forkCount
          pullRequests {pullRequests: totalCount}
          stargazers {stars: totalCount}
          totalIssues: issues {totalIssues: totalCount}
          openIssues: issues(states:[OPEN]) {openIssues: totalCount}
          primaryLanguage {primaryLanguage: name}
          languages(first: 3) { nodes {name} }
          repositoryTopics(first: 12) {nodes {topic {name}}}
       }
      }
    }
  }
}

Query variables
{
  "queryString": "GraphQL language:Go stars:>10 forks:>3 size:>2000 pushed:>=2018-08-08", 
  "numberRepos": 10 
}
