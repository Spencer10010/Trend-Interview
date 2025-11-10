# To run docker container:
- Be within the directory containing this README.md file
- docker-compose up --build
- Go to http://localhost:4000 to see the live site!

# Where to work on the Github Pages?
- The place that matters for development with this website is within this directory, the subdirectories is mainly made up of libraries that don't need modification
- index.md is the primary page holding the content and represents the homepage
- classification_and_regression.md is the second page containing my work for working on a traditional machine learning challenge
- bert_and_rnn.md is the third page where I tackle more complex models for a dataset that requires NLP models, I used prebuilt BERT models and created my own RNNs to see how they would perform
- default.html inside _layouts can change some of the website's formatting, created a navbar there
- style.css under assets\css can be used to style specific parts of the website such as adding the drop shadow on the navbar
- _config.yml contains the title of the webpage