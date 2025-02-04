# My-first
Welcome to Education by Avinash Singh! 🎓  This channel is your ultimate destination for mastering NEET &amp; JEE preparation along with concepts of Class 9, 10, 11, and 12. 
mkdir full-stack-app
cd full-stack-app
npm init -y
npm install express mongoose cors
const express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');

const app = express();
const port = 5000;

// Middleware
app.use(cors());
app.use(express.json());

// MongoDB connection
mongoose.connect('mongodb://localhost:27017/educationDB', {
    useNewUrlParser: true,
    useUnifiedTopology: true,
})
.then(() => console.log('Connected to MongoDB'))
.catch((err) => console.log(err));

// Simple API endpoint
app.get('/', (req, res) => {
    res.send('Welcome to Education by Avinash Singh API!');
});

app.listen(port, () => {
    console.log(`Server is running at http://localhost:${port}`);
});const mongoose = require('mongoose');

const studentSchema = new mongoose.Schema({
    name: { type: String, required: true },
    age: { type: Number, required: true },
    email: { type: String, required: true, unique: true },
});

const Student = mongoose.model('Student', studentSchema);

module.exports = Student;
npx create-react-app client
cd clientnpm install axios
