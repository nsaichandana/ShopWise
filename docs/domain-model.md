# ShopWise Domain Model

## Core Entities

* User
* RequirementProfile
* Laptop
* Recommendation
* RecommendationResult
* RecommendationReason

## Relationships

User 1 ──── * RequirementProfile

RequirementProfile 1 ──── * Recommendation

Recommendation 1 ──── * RecommendationResult

RecommendationResult * ──── 1 Laptop

RecommendationResult 1 ──── * RecommendationReason

## Notes

### User

Represents a registered user of ShopWise.

### RequirementProfile

Stores a user's requirements such as budget, coding preference, gaming preference, portability preference, and battery importance.

### Laptop

Represents a laptop available for recommendation.

### Recommendation

Represents a recommendation session generated for a requirement profile.

### RecommendationResult

Represents a single recommended laptop within a recommendation session.

Contains:

* Match score
* Ranking position

References:

* Laptop

### RecommendationReason

Represents an explanation for why a laptop was recommended.

Examples:

* Fits budget
* Good battery life
* Lightweight for daily travel
* Suitable for coding
