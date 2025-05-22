
# E-commerce Product Uploader

A full-stack web application that allows store owners to upload and manage product data. The application supports bulk upload via CSV/Excel files and manual CRUD operations.

## Features

- Upload product data in bulk using CSV or Excel files
- Manually add, edit, and delete products
- Paginated product listing with search functionality
- Image upload with validation
- Responsive UI for both desktop and mobile

## Technologies Used

- **Frontend**: React, TypeScript, TailwindCSS, shadcn/ui
- **Backend**: Node.js, Express
- **File Processing**: Multer, xlsx, csv-parser
- **Validation**: Zod

## Setup and Running Locally

### Prerequisites

- Node.js (v14 or later)
- npm or yarn

### Installation

1. Clone the repository
2. Install frontend dependencies:
   ```bash
   npm install
   ```

3. Navigate to the server directory and install backend dependencies:
   ```bash
   cd src/server
   npm install
   ```

### Running the Application

1. Start the backend server:
   ```bash
   cd src/server
   npm start
   ```
   This will start the server on port 3001.

2. In a new terminal, start the frontend development server:
   ```bash
   npm run dev
   ```
   This will start the React application on port 8080.

3. Open your browser and navigate to `http://localhost:8080`

## Usage

### Bulk Upload Products

1. Go to the "Bulk Upload" tab
2. Download a template (CSV or Excel)
3. Fill in the template with your product data
4. Upload the completed template
5. Review the upload results

### Manually Add Products

1. Click on "Add Product" button
2. Fill in the product details (name, description, price)
3. Upload a product image (JPG or PNG, max 5MB)
4. Click "Add Product" to save

### Search Products

Use the search bar to find products by name or description.

## File Templates

The application provides templates for both CSV and Excel formats. Each template includes the following columns:

- `name` (required): The product name
- `description` (required): A detailed description of the product
- `price` (required): The product price (must be a positive number)
- `image`: The image filename (for reference only, actual images must be uploaded separately)

## Validation

The application performs the following validations:

- Required fields (name, description, price) must be present
- Price must be a positive number
- Only JPG and PNG images are accepted
- Image file size must be less than 5MB
- No duplicate image files for different products
- No image URLs allowed (only uploaded files)
- Basic inappropriate content filtering

## License

This project is released under the MIT License.
