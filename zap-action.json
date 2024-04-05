const options = {
  url: 'https://app.cicerodata.com/v3.1/official',
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'X-KEY': bundle.authData.key
  },
  params: {
    'search_postal': bundle.inputData.search_postal,
    'search_country': bundle.inputData.search_country,
    'key': bundle.authData.key,
    'format': 'json'
  }
}

return z.request(options)
  .then((response) => {
    response.throwForStatus();
    const results = response.json.response.results.candidates[0].officials;
  
    return results;
  });
