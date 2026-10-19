# MarketLane

MarketLane is a lightweight local e-commerce application designed for small towns and community-focused regions. The platform lets users browse local businesses, search by category, view store details, and save favorites. Business owners can upload and manage basic listings through a simple admin interface. MarketLane focuses on speed, clarity, and easy deployment for small-scale environments.

| Topic  | Description |
| ------------- | ------------- |
| Requirement Statements | [Markdown](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/RequirementStatements.md)  |
| Use Cases | [PDF](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/UseCase.pdf)  |
| User Story Map | [Markdown](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/UserStories.md) |
| Class Diagram | [PNG](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/ClassDiagram.png) |
| Sequence Diagram | [PNG](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/SequenceDiagram.png) |

| Architecture | Description |
| ------------- | ------------- |
| System Context | [PDF](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/SystemContext.pdf) |
| Container Diagram | [PDF](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/ContainerDiagram.pdf) |
| Component Diagram | [PDF](https://github.com/hvo11152021/MarketLane/blob/main/design-diagrams/early-designs/ComponentDiagram.pdf) |


## Description

MarketLane helps locals in Fairfield to connect with its community.  
Users can quickly search items, explore store pages, and discover local promotions.  
The app provides essential marketplace features without complex integrations.  

## Members

**Hy Vo:** Project Owner

## Installation Instructions

Prerequisites: Java 21, Node.js 22.12 or later with npm, and Docker with Docker Compose.

1. From the project root, start the MySQL database:

   ```bash
   docker compose up -d mysql
   ```

2. Once MySQL is ready, start the backend (macOS/Linux):

   ```bash
   cd backend
   SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3307/marketlane_db \
   SPRING_DATASOURCE_USERNAME=arketlane-user \
   SPRING_DATASOURCE_PASSWORD=arketlane-pass \
   sh ./mvnw spring-boot:run
   ```

   These settings match the local Docker database. The backend runs at `http://localhost:8090`.

3. In a new terminal, from the project root, install and start the frontend:

   ```bash
   cd frontend
   npm install
   npm run dev
   ```

4. Open the URL printed by Vite, usually `http://localhost:5173`.

## Usage

https://youtu.be/p7IM0t6uTSQ

## Core Features (MVP)

- Business directory 
- Category-based search and filters  
- Store detail pages (hours, contact, photos, location link)  
- Favorites / bookmarks  
- Simple admin upload form for new business entries  

## Tech Stack

- **Frontend:** React + TypeScript  
- **Backend:** Spring Boot
- **Database:** mySQL
- **Deploy:** AWS
- **Auth:** Basic JWT (for admin upload)

## Contribution

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
