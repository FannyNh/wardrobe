# Spec

`Hi ! i'm a developper and i want to create a new webapp using AI with vide coding with codex. BUT before that i need to prepare all the spec. please give me the list of thing's that need to be done.`

---

## Purpose and Use Cases

### Core Objective
 - E-Wardrobe Management: Users can digitally store their wardrobe inventory, organizing clothes by type, color, season, etc.
 - Outfit Recommendations: AI-driven suggestions for outfits based on existing wardrobe items, weather, and user preferences.
 - Shopping Assistance: AI can propose clothing items to buy that complement the user's wardrobe and style preferences.

### Target Users

- Fashion Enthusiasts: People who are interested in personal styling, wardrobe management, and outfit creation.
- Professionals in the Fashion Industry: Designers, stylists, and fashion enthusiasts who want to organize, analyze, and showcase wardrobe options.

### User Stories / Use Cases

- As a User, I want to add clothes to my digital wardrobe so I can manage them easily.
- As a User, I want to receive AI-generated outfit suggestions so I can make better clothing choices.
- As a User, I want the AI to suggest new clothes that fit my style and current wardrobe.

### Key Features

Wardrobe Management:

- Upload and organize clothing items.
- Tag clothes by type, color, fabric, season, etc.

Outfit Generation:

- AI suggests outfits based on selected wardrobe items.
- Filter outfits by occasion, weather, or style preferences.

Personal Avatar:

- AI generates a personalized avatar based on the user's body type.
- Show outfits on the avatar to visualize fit and look.

Shopping Integration:

- Recommend clothes to purchase, including links to online stores.
- Users can “like” or “save for later” suggestions.

Customizable User Profiles:

- Users can set their preferences (e.g., color preferences, styles, sizes).
- Users can set their style goals (e.g., casual, formal, seasonal).
- add clothe in e-wardrobe
- can select the type on clothe
- AI-driven proposition of outfit 
- AI generated avatar with the outfit

## User Flow

User Onboarding:

- Create an account or sign in.
- Complete basic profile (e.g., size, style preferences).
- Upload initial wardrobe inventory or browse example items.

Adding Clothes:

- Upload clothes manually (image or name), or sync with external wardrobe apps.
- Classify clothes by type, size, and color.

Outfit Suggestions:

- AI suggests outfits based on selected items, preferences, and occasions.
- User reviews and customizes outfits.

Shopping Recommendations:

- Based on the current wardrobe and style preferences, suggest purchase options.

Avatar Visualization:

- View outfits on a digital avatar to assess fit and look.

---

## Technical Requirements

### Tech Stack

#### Frontend:

- Framework: Vue.js (Vue 3)
- State Management: Pinia
- Builder: Vite
- Testing: Vitest
- Mocking: Mock Service Worker
- Styling: TailwindCSS
- Code Quality: ESLint, Prettier
- TypeScript: Strongly typed, object-oriented structure
- Quality Assurance: Sonar for code quality and security checks

#### Backend:

- Framework: Spring Boot (Java 21)
- Data Modeling: MapStruct, Lombok for POJO generation
- Database: PostgreSQL for persistent storage
- Dependency Management: Maven
- Testing: Mockito for unit testing
- Security: Spring Security (if user accounts are required)
- API: RESTful or GraphQL depending on frontend needs

#### AI:

- AI Engine: OpenAI Codex (for generating clothing suggestions, avatars, etc.)
- Integration: Codex API integration for backend logic
- Avatar Generation: Integration with AI-based avatar generation models, possibly leveraging deep learning for accurate body shape rendering.

---

## System Architecture

### Frontend:

- Vue.js communicates with the backend via REST APIs or GraphQL for dynamic content.
- TailwindCSS for responsive and quick UI styling.
- Vuex/Pinia to manage global state (e.g., wardrobe, preferences, avatars).

### Backend:

- Spring Boot with Java 21 for scalable microservices architecture.
- Database schema for storing user profiles, clothing inventory, outfit suggestions, etc.
- Codex integration on the backend for generating outfit suggestions and personalized avatars.

### AI Services:

- Codex as a key AI-driven service for generating text-based suggestions.
- Avatar generation service: Integrate a pre-trained deep learning model for creating avatars.

### Security:

- User authentication using Spring Security (OAuth2, JWT).
- Input validation and authorization checks for all user-generated content (e.g., wardrobe items).

### Third-Party Integrations:

- E-commerce API (for shopping suggestions and links).
- Cloud services for AI processing (AWS, Google Cloud AI, etc.).

---

## Dev rules 

`Follow the principles of clean code and maintain a high level of readability.`

- Follow DDD method:
  - Structure backend around the business domain (Wardrobe, Outfit, User, etc.).
  - Ensure the frontend maintains a clear separation of concerns (e.g., components for adding items, generating outfits).
- Meaningful Names
- Functions Should Do One Thing
- Keep Functions Small
- Avoid Side Effects
- Avoid Magic Numbers
- Single Responsibility Principle
- Open/Closed Principle
- Avoid Duplication
- Error Handling
- Avoid Long Method Chains
- Use Design Patterns
- Encapsulate What Varies

---

## Testing Strategy

### Unit Tests:

- Write unit tests for individual functions and methods using tools like JUnit, Vitest, and Mockito.

### Integration Tests:

- Test interaction between system components (e.g., frontend-backend communication, Codex integration).

### End-to-End Tests:

- Simulate user behavior using tools like Cypress or Selenium to test the full application flow.

### Load Testing:

- Test system scalability and load capacity, especially for AI services, to ensure quick response times for outfit suggestions.