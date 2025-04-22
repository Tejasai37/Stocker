# Stocker

A web-based stock portfolio application built with Flask and deployed on AWS.

## Overview

Stocker is a comprehensive stock portfolio tracking application that allows users to:
- Create and manage their account
- Track their stock investments
- Buy and sell stocks
- Receive notifications for account activities

## Tech Stack

- **Backend**: Flask (Python)
- **Database**: AWS DynamoDB
- **Authentication**: Custom implementation with AWS SNS notifications
- **Deployment**: AWS EC2
- **Notifications**: AWS SNS

## Features

- **User Authentication**: Secure login and registration system
- **Portfolio Management**: Track all your investments in one place
- **Buy/Sell Interface**: Easy-to-use interface for stock transactions
- **Real-time Notifications**: Get alerts for account activities and stock updates


## Installation and Local Development



### Setup

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/stocker.git
   cd stocker
   ```

2. Set up a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Configure AWS credentials:
   ```
   aws configure
   ```

5. Set up environment variables:
   ```
   export FLASK_APP=app.py
   export FLASK_ENV=development
   export AWS_REGION=your-aws-region
   ```

6. Run the application:
   ```
   flask run
   ```

## AWS Deployment

### EC2 Setup

1. Launch an EC2 instance with Amazon Linux 2
2. Configure security groups to allow HTTP/HTTPS traffic
3. SSH into your instance:
   ```
   ssh -i your-key.pem ec2-user@your-instance-ip
   ```
4. Install dependencies:
   ```
   sudo yum update -y
   sudo yum install git python3 python3-pip -y
   ```
5. Clone the repository and set up as in the local development steps

### DynamoDB Setup

1. Create the necessary tables through AWS Console or CLI:
   - Users table
   - Stocks table
   - Transactions table
   - Portifolio table

2. Ensure your EC2 instance has an IAM role with permissions to access DynamoDB

### SNS Configuration

1. Create SNS topics for:
   - User authentication notifications
   - Stock transaction notifications

2. Set up appropriate subscriptions for email/SMS notifications

## Environment Variables

The following environment variables need to be configured:

- `AWS_ACCESS_KEY_ID`: Your AWS access key
- `AWS_SECRET_ACCESS_KEY`: Your AWS secret key
- `AWS_REGION`: AWS region (e.g., us-east-1)
- `DYNAMODB_USERS_TABLE`: Name of the DynamoDB users table
- `DYNAMODB_STOCKS_TABLE`: Name of the DynamoDB stocks table
- `DYNAMODB_TRANSACTIONS_TABLE`: Name of the DynamoDB transactions table
- `DYNAMODB_PORTIFOLIOS_TABLE`: Name of the DynamoDB transactions table
- `SNS_AUTH_TOPIC_ARN`: ARN for the authentication SNS topic
- `SNS_TRANSACTION_TOPIC_ARN`: ARN for the transaction SNS topic
- `SECRET_KEY`: Flask secret key for session management

## Project Structure

```
stocker/
├── app.py              # Application entry point
├── setup_dynamodb.py
├── requirements.txt    # Python dependencies
├── static/             # Static files (CSS, JS)
├── templates/          # HTML templates

```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or support, please contact [your-email@example.com](mailto:your-email@example.com).
