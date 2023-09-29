# Always Encrypted in MVC Project with SQL Server

This repository provides guidance and code samples for implementing Always Encrypted in an MVC (Model-View-Controller) project that uses Microsoft SQL Server for data storage. Always Encrypted is a security feature that ensures sensitive data remains encrypted, even when accessed by authorized users.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Configuration Steps](#configuration-steps)
- [Code Samples](#code-samples)
- [Testing](#testing)
- [Key Management](#key-management)
- [Resources](#resources)
- [Contributing](#contributing)

## Prerequisites

Before you begin, ensure you have the following prerequisites in place:

- **Microsoft SQL Server**: You should have a SQL Server instance where your database resides.

- **SQL Server Management Studio (SSMS)**: To configure and manage Always Encrypted, SSMS is a useful tool.

- **SQL Server Data Tools (SSDT)**: SSDT is beneficial for database schema changes.

- **Visual Studio or Visual Studio Code**: These development environments are required for working on your MVC project.

## Configuration Steps

Follow these steps to implement Always Encrypted in your MVC project:

1. **Database Configuration**:
   - Create a SQL Server database or select an existing one for your project.
   - Identify the columns that contain sensitive data and need encryption.
   - Use SSMS or SSDT to configure Always Encrypted for these columns. This includes generating Column Master Keys and Column Encryption Keys.

2. **Development**:
   - In your MVC project, ensure you have references to appropriate libraries like `System.Data.SqlClient`.
   - Modify your data access layer to work with encrypted columns.
   - Use parameterized queries when interacting with encrypted columns to ensure the data is encrypted on the client side.

3. **Connection Strings**:
   - Update your connection string in the MVC project to include `Column Encryption Setting=enabled`.

4. **Column Encryption in Code**:
   - Implement code to encrypt data before inserting or updating sensitive information in the database.
   - Similarly, implement code to decrypt data when retrieving it from the database.

5. **Testing**:
   - Test your application thoroughly to ensure data encryption and decryption are working correctly.
   - Verify that only authorized users and applications can access decrypted data.

6. **Key Management**:
   - Ensure that Column Master Keys are stored securely outside the database, such as in Azure Key Vault or an HSM.
   - Establish proper access controls for managing the keys.

## Code Samples

In the `code-samples` directory of this repository, you will find sample code demonstrating how to encrypt and decrypt data in your MVC project using Always Encrypted.

## Testing

Use the sample code and test cases provided in this repository to validate the proper functioning of Always Encrypted in your MVC project. Ensure that sensitive data remains encrypted and secure.

## Key Management

Proper key management is essential for the security of your encrypted data. Follow best practices for storing and managing Column Master Keys to prevent unauthorized access.

## Resources

Here are some helpful resources for working with Always Encrypted in MVC projects with SQL Server:

- [Microsoft Documentation on Always Encrypted](https://docs.microsoft.com/en-us/sql/relational-databases/security/encryption/always-encrypted-database-engine)

- [SQL Server Always Encrypted - Best Practices](https://docs.microsoft.com/en-us/sql/relational-databases/security/encryption/always-encrypted-best-practices)

- [Using Always Encrypted in a .NET Application](https://docs.microsoft.com/en-us/sql/relational-databases/security/encryption/always-encrypted-walkthrough-always-encrypted)

## Contributing

Contributions to this repository are welcome! If you have code samples, improvements, or additional resources to share, please feel free to submit pull requests.

