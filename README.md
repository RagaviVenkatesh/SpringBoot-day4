Spring Boot Day 4 Exercise
Exercise Title: Introduce DTO and ModelMapper

Objective:

Today you will separate your internal entity (User) from the API response and request using DTOs.
You will also integrate ModelMapper to map between User and UserDTO automatically.

Requirements:

1. Create a new class UserDTO with fields: id, name, and email.
2. Do not expose the entity directly from the controller.
3. Install ModelMapper dependency in pom.xml:
   
 <dependency>
 <groupId>org.modelmapper</groupId>
 <artifactId>modelmapper</artifactId>
 <version>3.1.1</version>
 </dependency>
 
5. Configure a ModelMapper bean in your configuration class.
6. Convert Entity to DTO in GET response using ModelMapper.
7. Convert DTO to Entity in POST/PUT request using ModelMapper.
8. Update your controller to use DTOs in all API methods.
9. 
Bonus Task (Optional):

Add a field maskedEmail to UserDTO which returns the email with domain hidden. Example:
user@example.com becomes user@****.com. Use a utility method to populate it during mapping.

Submission Checklist:

- UserDTO created and used in controller
- Entity-to-DTO and DTO-to-Entity mapping works via ModelMapper
- Controller no longer exposes internal entity
- Bonus logic implemented (if attempted)
