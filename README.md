# codepipeline-S3-memorygame
# Memory Matching Game with AWS Continuous Deployment
This project showcases a simple memory matching game, built with HTML, CSS, and JavaScript, and deployed using AWS S3 and AWS CodePipeline for continuous integration and deployment.

# TL;DR
This repository contains the source code for a memory matching game. The project is continuously deployed using AWS CodePipeline. The game is hosted on an AWS S3 bucket set up for static website hosting. The CodePipeline is configured to automatically deploy any updates from this GitHub repository to the S3 bucket.

# The Game
This memory matching game challenges the user to match pairs of images. Here's how it works:

The user clicks two cards (images of memes) to try to match them.
If the cards match, they disappear from the board.
If the cards don't match, they flip back to their blank side, and the user tries again.
## Features to be Added
* Scoring mechanism
* Timer for game completion
* Additional cards for increased difficulty
* Multi-player mode for score comparison
# The Deployment Environment
The game is hosted in an AWS S3 bucket configured for static website hosting. The deployment process is automated through AWS CodePipeline.

# The Deployment Pipeline
We use AWS CodePipeline to create a CI/CD pipeline:

* Source: The pipeline is triggered whenever a change is detected in this GitHub repository.
* Build: Any new changes are prepared for deployment.
* Deploy: The changes are deployed to the S3 bucket hosting the game.

# Prerequisites
+ AWS account (eligible for Free Tier) 
+ GitHub repository containing the game code
+ AWS S3 bucket for static website hosting
+ AWS CodePipeline for continuous deployment
+ AWS Free Tier and Costs
While the services used (S3, CodePipeline) are eligible for the AWS Free Tier, it's important to monitor your usage, as charges may be incurred over time. It is recommended to shut down resources after finishing the deployment.

# How to Set Up the Project
1. Set Up S3 for Static Website Hosting
   * Create an S3 bucket and configure it for static website hosting.
   * Upload your game files (HTML, CSS, JavaScript) to the bucket.
   * Note the S3 URL where your static website will be hosted.

2. Set Up AWS CodePipeline
   * Create a pipeline in AWS CodePipeline.
   * Connect the pipeline to your GitHub repository.
   * Define the build and deploy stages. Set S3 as the deployment target.
   * Every time you push changes to the GitHub repository, the CodePipeline will automatically update your game on S3.
# How to Contribute
Feel free to fork this repository and contribute new features (such as scoring, multiplayer, etc.) by submitting pull requests.

