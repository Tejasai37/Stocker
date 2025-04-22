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


## Project Structure

```
stocker/
├── app.py              # Application entry point
├── requirements.txt    # Python dependencies
├── static/             # Static files (CSS, JS)
├── templates/          # HTML templates
├── setup_dynamodb.py   # Database setup file

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
