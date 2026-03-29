# Hydro-Tech Smart Water Management

## Current State
Login page has Sign In + Demo button. After login, users go directly to Dashboard with no profile requirement.

## Requested Changes (Diff)

### Add
- ProfileSetup step after login: required fields Full Name, Phone, Location, Organization
- Block all navigation until profile is complete
- Persist completion in localStorage

### Modify
- Remove Demo button from LoginPage
- App flow: Login -> ProfileSetup (if needed) -> Dashboard

### Remove
- Demo/guest login button

## Implementation Plan
1. Remove Continue as Demo button from LoginPage
2. Add profileComplete state initialized from localStorage
3. Add ProfileSetupPage component with required form fields
4. Show ProfileSetupPage after login if profile not complete
5. On submit, save to localStorage and proceed to dashboard
