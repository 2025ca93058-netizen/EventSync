# EventSync - Sprint 1 MVP (Basic Version)

**Simple Event Management Platform**  
**Sprint:** 1 (MVP - Minimum Viable Product)  
**Status:** Working Software - Ready for Demo

# EventSync - Sprint 2 Final Product

**Simple Event Management Platform**  
**Sprint:** 2 (FInal Product)  
**Status:** Working Software

---

## What's Included (Sprint 1 Features)

This is a **basic, working version** with core functionality only:

### ✅ Feature 1: View Event Listings (US-001)
- Display 6 sample events in a grid
- Shows title, date, time, location, organizer
- Color-coded seat availability (green/orange/red)
- Click to view details

### ✅ Feature 2: View Event Details (US-002)
- Modal popup with full event information
- Shows all event details
- Register button (or "Event Full" if no seats)

### ✅ Feature 3: Register for Event (US-003)
- Simple registration form (name, email, phone)
- Form validation (10-digit phone number required)
- Prevents duplicate registrations
- Success message after registration
- Seat count updates in real-time

### ✅ Feature 4: Participant Dashboard (US-004)
- View all your registrations
- Shows total registration count
- Displays registration details for each event
- Empty state if no registrations

---

## What's NOT Included (Sprint 2 Features)

These will be added in Sprint 2 based on feedback:

❌ Search functionality  
❌ Filter by category  
❌ Filter by availability  
❌ Cancel registration  
❌ Loading states  
❌ Advanced error messages

---

## How to Run

### Option 1: Python (Easiest)

```bash
# Navigate to the code folder
cd eventsync-sprint1-basic/code/

# Start server
python -m http.server 8000

# Open browser
# Visit: http://localhost:8000
```

### Option 2: Node.js

```bash
cd eventsync-sprint1-basic/code/
npx http-server -p 8000
# Visit: http://localhost:8000
```

### Option 3: Just Open in Browser

- Simply open `index.html` in your web browser
- Works directly (no server needed for basic functionality)

---

## How to Test

### Test Flow 1: Browse and Register

1. Open `index.html` in browser
2. You'll see 6 events displayed
3. Click on any event (e.g., "Web Development Bootcamp")
4. Event details modal opens
5. Click "Register Now"
6. Fill in the form:
   - Name: John Doe
   - Email: john@example.com
   - Phone: 9876543210
7. Click "Register"
8. Success message appears
9. Available seats decrease by 1

### Test Flow 2: View Dashboard

1. Click "My Events" in navigation
2. You'll see your registration
3. Check that all details are correct
4. Statistics show "1" total registration

### Test Flow 3: Multiple Registrations

1. Go back to "Events"
2. Register for 2-3 more events
3. Check dashboard shows all registrations
4. Each event shows "Confirmed" status

### Test Flow 4: Duplicate Prevention

1. Try to register for the same event again
2. Use the same email
3. System shows: "You are already registered for this event!"

### Test Flow 5: Full Event

1. Note which events have limited seats (orange)
2. Register multiple times until seats = 0
3. Event shows "Event Full" button (disabled)
4. Cannot register anymore

---

## Technical Details

### Technology Stack
- **HTML5** - Structure
- **CSS3** - Styling (responsive)
- **JavaScript (Vanilla)** - Functionality
- **localStorage** - Data persistence

### Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### File Structure
```
code/
├── index.html              # Homepage (event listing)
├── dashboard.html          # My Events page
├── css/
│   └── styles.css          # All styling
└── js/
    ├── events.js           # Data & utilities
    ├── app.js              # Main app logic
    └── dashboard.js        # Dashboard logic
```

### Data Storage

All data stored in browser's localStorage:
- `events` - List of all events
- `registrations` - User registrations

**Note:** Data is browser-specific. Clearing browser data will reset the app.

---

## Features in Detail

### 1. Event Listing (index.html)

**Display:**
- Grid layout (3 columns on desktop, 1 on mobile)
- Each card shows:
  - Event title
  - Date, time, location, organizer
  - Available seats with color coding

**Seat Colors:**
- 🟢 Green: 6+ seats available
- 🟠 Orange: 1-5 seats (limited)
- 🔴 Red: 0 seats (full)

### 2. Event Details Modal

**Opens when:** User clicks on event card

**Shows:**
- All event information
- Full description
- Capacity and available seats
- Register button

### 3. Registration Form

**Fields:**
- Name (required, min 2 characters)
- Email (required, valid format)
- Phone (required, exactly 10 digits)

**Validation:**
- Client-side HTML5 validation
- Phone number regex: `[0-9]{10}`
- Duplicate check by email + event ID
- Seat availability check

### 4. Dashboard (dashboard.html)

**Shows:**
- Total registrations count
- List of all registered events
- Registration details for each
- Empty state if no registrations

---

## Sample Data

The app comes with 6 pre-loaded events:

1. **Web Development Bootcamp** - Tech Hub, Mumbai (50 seats)
2. **Digital Marketing Workshop** - Business Center, Pune (30 seats)
3. **AI & Machine Learning Seminar** - Innovation Lab, Bangalore (40 seats)
4. **Startup Networking Event** - Co-working Space, Delhi (60 seats)
5. **Photography Masterclass** - Art Studio, Chennai (25 seats)
6. **Data Science Conference** - Convention Center, Hyderabad (100 seats)

---

## Known Limitations (Sprint 1)

### By Design (MVP Scope):
- No backend server (localStorage only)
- No user authentication
- No search or filter
- No email notifications
- Cannot cancel registrations
- Data is browser-specific (not synced across devices)

### Acceptable for Sprint 1:
- Basic styling (not polished)
- Simple error messages
- No loading indicators
- Manual testing only

---

## Testing Checklist

Use this to verify everything works:

- [ ] Events display on homepage
- [ ] Event cards are clickable
- [ ] Event details modal opens
- [ ] Register button works
- [ ] Form validation works
- [ ] Cannot enter letters in phone field
- [ ] Cannot submit empty form
- [ ] Success message appears after registration
- [ ] Seat count decreases after registration
- [ ] Dashboard shows registrations
- [ ] Dashboard statistics are correct
- [ ] Cannot register twice for same event
- [ ] Cannot register when event is full
- [ ] Works on mobile (responsive)

---

## Sprint 1 Metrics

**Development Time:** ~20 hours (estimated)

**Code Stats:**
- HTML: ~180 lines
- CSS: ~350 lines
- JavaScript: ~280 lines
- **Total:** ~810 lines

**User Stories Completed:** 4/5 (80%)
- ✅ US-001: View Event Listings
- ✅ US-002: View Event Details
- ✅ US-003: Register for Event
- ✅ US-004: Participant Dashboard
- ⏳ US-005: Create New Event (deferred to Sprint 2)

---

## Next Steps (Sprint 2)

Based on Sprint 1 demo feedback, Sprint 2 will add:

1. **Search functionality** - Find events by keyword
2. **Filter by category** - Technology, Business, Arts, etc.
3. **Cancel registration** - Give users control
4. **Enhanced UX** - Loading states, better messages
5. **Complete testing** - Comprehensive test cases

---

## For Evaluators

### Quick Demo (5 minutes):

1. **Start:** Open index.html
2. **Browse:** See 6 events displayed
3. **View:** Click "Web Development Bootcamp"
4. **Register:** Fill form and submit
5. **Check:** Go to "My Events" dashboard
6. **Verify:** Registration appears

### Evaluation Criteria Met:

✅ **Working software** - Fully functional  
✅ **Basic features** - Core functionality implemented  
✅ **Limited scope** - Appropriate for Sprint 1 MVP  
✅ **Demonstrates Agile** - Iterative approach  
✅ **Ready for feedback** - Can be enhanced in Sprint 2

---

## Support

### If Something Doesn't Work:

1. **Clear browser cache** - Hard refresh (Ctrl+Shift+R)
2. **Check console** - Open browser DevTools (F12)
3. **Reset data** - Clear localStorage:
   ```javascript
   // In browser console
   localStorage.clear();
   location.reload();
   ```
4. **Try different browser** - Test in Chrome/Firefox

---

## License

Academic Project - BITS Pilani WILP  
Course: Agile Software Processes  
Sprint: 1 (MVP)

---

**Status:** ✅ WORKING - READY FOR SPRINT 1 DEMO  
**Version:** 1.0 (Basic MVP)  
**Date:** February 13, 2026

---

**This is the Sprint 1 baseline.** Sprint 2 will build upon this foundation with enhanced features based on stakeholder feedback.
