# Visual Scoring & Report Generation Dashboard

A secure, self-serve dashboard for uploading visuals, scoring them, and generating detailed reports with insights and recommendations. Built with FastAPI and React, this enterprise-grade solution provides powerful scoring capabilities with automated report generation.

## 🌟 Features

- 🔐 **Secure Authentication & Role-based Access**
  - JWT-based authentication
  - Role-based permissions (Admin/User)
  - Multi-factor authentication support
  - Session management

- 📊 **Visual Scoring System**
  - 10 customizable scoring criteria
  - 1-10 scale scoring
  - Real-time validation
  - Comparative analysis
  - Historical tracking

- 📑 **Dynamic Report Generation**
  - PDF report generation
  - Customizable templates
  - Automated insights
  - Performance trends
  - Export functionality

- 👑 **Admin Dashboard**
  - User management
  - System monitoring
  - Analytics dashboard
  - Content management
  - Audit logs

- ☁️ **AWS Integration**
  - S3 for file storage
  - RDS for database
  - Cognito for authentication
  - CloudFront for content delivery
  - Lambda for serverless functions

- 🛡️ **Enterprise-grade Security**
  - End-to-end encryption
  - GDPR compliance
  - Regular security audits
  - Data backup
  - Access logging

- 💳 **Payment & Subscription System**
  - Secure payment processing (Stripe)
  - Multiple subscription tiers
  - Usage-based billing
  - Payment history
  - Invoice generation
  - Automatic renewals

## 🏗️ Project Structure

```plaintext
project/
├── backend/
│   ├── app/
│   │   ├── auth/                 # Authentication & authorization
│   │   ├── scoring/              # Scoring logic
│   │   ├── reports/              # Report generation
│   │   ├── admin/               # Admin functionalities
│   │   └── core/                # Core utilities
│   ├── main.py                  # FastAPI application
│   ├── requirements.txt         # Python dependencies
│   └── alembic/                 # Database migrations
├── frontend/
│   ├── src/
│   │   ├── components/          # Reusable components
│   │   ├── pages/              # Page components
│   │   ├── services/           # API services
│   │   ├── theme.ts            # MUI theme
│   │   └── App.tsx             # Main application
│   └── package.json            # Node dependencies
└── docker/                     # Docker configuration
```

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Node.js 16+ / React Typescript
- PostgreSQL
- AWS Account
- Docker & Docker Compose (optional)

### Environment Setup

1. **Clone the Repository**
```bash
git clone https://github.com/yourusername/visual-scoring-dashboard.git
cd visual-scoring-dashboard
```

2. **Backend Setup**
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. **Frontend Setup**
```bash
cd frontend
npm install
```

4. **Environment Variables**

Create `.env` files in both backend and frontend directories:

```bash
# Backend (.env)
DATABASE_URL=postgresql://user:password@localhost:5432/db
AWS_ACCESS_KEY=your_access_key
AWS_SECRET_KEY=your_secret_key
JWT_SECRET=your_jwt_secret

# Frontend (.env)
VITE_API_URL=http://localhost:8000
```

### Running the Application

1. **Start Backend**
```bash
cd backend
uvicorn main:app --reload
```

2. **Start Frontend**
```bash
cd frontend
npm run dev
```

3. **Access the Application**
- Frontend: http://localhost:3000
- API Documentation: http://localhost:8000/docs

## 📝 API Documentation

### Authentication Endpoints
- POST `/api/auth/register` - User registration
- POST `/api/auth/login` - User login
- POST `/api/auth/refresh` - Refresh token

### Scoring Endpoints
- POST `/api/scoring/upload` - Upload visual
- POST `/api/scoring/score` - Submit scores
- GET `/api/scoring/history` - Get scoring history

### Report Endpoints
- POST `/api/reports/generate` - Generate report
- GET `/api/reports/list` - List reports
- GET `/api/reports/{id}` - Get specific report

### Admin Endpoints
- GET `/api/admin/users` - List users
- GET `/api/admin/stats` - System statistics
- GET `/api/admin/logs` - System logs

### Payment Endpoints
- POST `/api/payments/create-subscription` - Create new subscription
- POST `/api/payments/cancel-subscription` - Cancel subscription
- GET `/api/payments/history` - Get payment history
- GET `/api/payments/invoices` - Get invoices
- POST `/api/payments/webhook` - Stripe webhook handler

## 🔒 Security Features

- JWT Authentication
- Role-based Access Control
- AWS S3 Secure File Storage
- Data Encryption
- HTTPS/SSL
- Input Validation
- Rate Limiting

## 🚀 Deployment

### Docker Deployment
```bash
docker-compose up -d
```

### Manual Deployment
1. Build frontend
```bash
cd frontend
npm run build
```

2. Start backend server
```bash
cd backend
gunicorn main:app
```

## 📈 Monitoring & Maintenance

- AWS CloudWatch for monitoring
- Regular security updates
- Database backups
- Performance optimization
- User support

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Support

For support, email support@visualscoring.com or join our Slack channel.

## 🙏 Acknowledgments

- FastAPI for the backend framework
- React for the frontend framework
- AWS for cloud services
- Material-UI for UI components


This README.md now provides:
- Detailed feature descriptions
- Complete project structure
- Clear setup instructions
- API documentation
- Security features
- Deployment instructions
- Monitoring & maintenance details
- Contributing guidelines
- License information
- Support channels
- Acknowledgments


