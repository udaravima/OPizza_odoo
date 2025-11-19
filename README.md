# Odoo Docker Project

This project contains a basic setup to run Odoo 19 with PostgreSQL using Docker.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* [Docker](https://docs.docker.com/get-docker/)
* [Docker Compose](https://docs.docker.com/compose/install/)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/opizza_odoo.git
   cd opizza_odoo
   ```

2. **Create a password file:**

   Create a file named `odoo_pg_pass` in the root directory and add a secure password for the PostgreSQL database.

   ```bash
   echo "your-super-secret-password" > odoo_pg_pass
   ```

3. **Build and run the containers:**

   ```bash
   docker-compose up -d
   ```

## Usage

After running `docker-compose up -d`, the Odoo instance will be available at [http://localhost:8069](http://localhost:8069).

The master password for this Odoo instance is `admin`. **It is strongly recommended to change this in a production environment.**

## Custom Addons

This project is configured to load custom addons from the `./addons` directory. Place your custom Odoo modules in this directory, and they will be available in the Odoo instance.

Currently, the following custom addons are included:
* **Odoo WhatsApp Integration**: This module integrates Odoo with WhatsApp.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
