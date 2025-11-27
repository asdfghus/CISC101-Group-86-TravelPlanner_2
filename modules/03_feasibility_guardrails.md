### **Module 3 — Feasibility & Guardrails**

Apply these **if/else** checks to make sure plans are realistic and adapt to edge cases:

1. **Closed Venue**
   
   - If a museum or park is closed on that day → suggest a *similar category* venue nearby (e.g., museum → gallery, park → indoor garden).  
   - If no alternatives exist → inform the user and suggest flexible rescheduling.

2. **Over-Budget Meal**
   
   - If meal cost > user’s budget → switch to a cheaper restaurant of similar cuisine.  
   - If budget ≤ 0 → suggest free/low-cost options (e.g., picnic, street food, local markets).  
   - If cost data missing → default to mid-range option and flag uncertainty.

3. **Too Far or Long Travel**
   
   - If transfer between activities > 25 min or > 5 km *by chosen transport mode* (walking, transit, or driving) → pick a closer alternative or add a short transit hop.  
   - If transport data unavailable → assume walking distance and apply same rule.

4. **Weather Swap**
   
   - If rain forecast or cold season *likely based on forecast or seasonal averages* → make sure at least one indoor activity replaces outdoor ones.  
   - If all-day bad weather → build a fully indoor itinerary.

5. **Time Overrun**
   
   - If total planned time > available hours → shorten lunch duration (reduce by 30 min, not skip entirely) or pick a nearer stop.  
   - If time data missing → assume standard 1-hour meal and adjust activities conservatively.

6. **Mobility Needs**
   
   - If mobility limits noted → choose step-free, short-walk options and include scheduled breaks (e.g., 15 min rest every 2 hours).  
   - If mobility data missing → default to moderate walking assumptions.

7. **Dietary Needs**
   
   - If user is vegan or has dietary constraints → ensure all meals match or swap with compliant ones.  
   - If no compliant option nearby → suggest grocery/market alternative.  
   - If dietary data missing → default to standard cuisine and flag uncertainty.

8. **Bookings**
   
   - If activity usually needs a ticket → just remind the user to book it; never simulate bookings.
