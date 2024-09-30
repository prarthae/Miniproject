# Mini Project

**Mess Connect** is a web application designed to streamline the process of ordering daily meals for college students. Students can select a registered mess, place daily orders, cancel them if necessary, and pay through Razorpay. Mess owners can also register their messes on the platform and provide meal details.

## Features

- **User Authentication:** College students and mess owners can register and log in to the platform.
- **Mess Registration:** Mess owners can register their mess and provide details such as menu, location, and timings.
- **Order Placement:** Students can search for messes and place orders for their daily meals.
- **Order Cancellation:** Orders can be canceled up to 24 hours before the scheduled meal.
- **Payment Integration:** Students can securely make payments via Razorpay.
- **Data Management:** MongoDB is used to store student profiles, mess details, orders, and payment transactions.

## Tech Stack

- **Node.js**: Backend framework.
- **Express.js**: Server-side framework for building APIs and handling routes.
- **EJS**: Templating engine for rendering dynamic views.
- **MongoDB**: NoSQL database for storing user, mess, and order data.
- **Razorpay**: Integrated payment gateway for handling transactions.



## Database Structure

- **Users Collection:**
  - Student and mess owner profiles, including name, email, password, and user type (student or owner).

- **Messes Collection:**
  - Registered mess details including name, address, menu, and owner information.

- **Orders Collection:**
  - Orders placed by students, including meal details, mess, student, order status, and cancellation status.

- **Payments Collection:**
  - Transaction history and payment status.

## How It Works

### Student Actions:
1. **Register/Login:** Students register or log in to the platform.
2. **Search for Mess:** Students can search for available messes based on location and meal preferences.
3. **Place Order:** Students select a mess and place their order.
4. **Cancel Order:** Orders can be canceled if done 24 hours in advance.
5. **Make Payment:** Payments are made securely using Razorpay.

### Mess Owner Actions:
1. **Register/Login:** Mess owners register and log in to manage their mess details.
2. **Add/Update Mess Details:** Mess owners can provide details about their mess, including the menu and operating hours.
3. **View Orders:** Owners can view and manage orders placed by students.

## Razorpay Integration

The application integrates with Razorpay for secure payment processing. The payment workflow involves:

1. Student places an order and proceeds to payment.
2. Razorpay handles the transaction and provides a payment status.
3. The order status is updated in the database based on the payment result.
