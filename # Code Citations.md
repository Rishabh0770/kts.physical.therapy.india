# Code Citations

## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('book
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('book
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('book
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/virajkadam/ultrasuedegreen.com/blob/8067a4667643b2405161501426328a84c434990d/mission_and_vision.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CD
```


## License: unknown
https://github.com/mohamedbirali/components/blob/4f4b9a8831a560325c217fa4ce46f0f878d22110/professeur.html

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdeliv
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error }
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error }
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error }
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot:', error);
      return false;
    }

    return !data;
  } catch (error) {
    console.error('❌ Unexpected error:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    const name = document.getElementById("bName").value.
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot:', error);
      return false;
    }

    return !data;
  } catch (error) {
    console.error('❌ Unexpected error:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    const name = document.getElementById("bName").value.
```


## License: unknown
https://github.com/redcentre/Carbon.Example.JSClient/blob/feb07c097370e3b5ec459bc066e69baef273268d/client.js

```
I'll provide complete, production-ready Supabase integration code. Replace the placeholders with your actual credentials.

## 1. ADD SUPABASE CDN (In `<head>` before closing tag)

```html
<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
```

---

## 2. FULL INTEGRATED JAVASCRIPT (Replace existing booking JavaScript in `<script>` tag)

```javascript
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // Replace with your key
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // Replace with your payment link

// Initialize Supabase client
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY STATUS
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    // Show loading state
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    // Fetch booked slots from Supabase
    const bookedSlots = await fetchBookedSlots(date);

    // Check if date is today
    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT TIME SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// VALIDATE APPOINTMENT DATE UNIQUENESS
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      // No record found - slot is available
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot availability:', error);
      return false;
    }

    // Record found - slot is booked
    return !data;
  } catch (error) {
    console.error('❌ Unexpected error checking slot:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING TO SUPABASE
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    // Get form values
    const name = document.getElementById("bName").value.trim();
    const phone = document.getElementById("bPhone").value.trim();
    const email = document.getElementById("bEmail").value.trim();
    const age = document.getElementById("bAge").value.trim();
    const date = document.getElementById("bDate").value;
    const timeValue = document.getElementById("bTime").value;
    const service = document.getElementById("bService").value;
    const message = document.getElementById("bMsg").value.trim();

    // ──────────────────────────────────────────────────────────
    // VALIDATION
    // ──────────────────────────────────────────────────────────
    if (!name || !phone || !date || !timeValue || !service) {
      showToast("⚠️ Please fill all required fields and select a time slot!", "#e53e3e");
      return;
    }

    // Validate phone number (10 digits)
    if (!/^\d{10}$/.test(phone.replace(/\D/g, ""))) {
      showToast("⚠️ Please enter a valid 10-digit phone number!", "#e53e3e");
      return;
    }

    // Extract time from timeValue (format: "HH:MM|Label")
    const [time, timeLabel] = timeValue.split("|");

    // ──────────────────────────────────────────────────────────
    // DOUBLE-BOOKING CHECK (CRITICAL)
    // ──────────────────────────────────────────────────────────
    const slotAvailable = await isSlotAvailable(date, time);
    if (!slotAvailable) {
      showToast("⚠️ This slot is already booked! Please select another.", "#e53e3e");
      // Refresh slots to show updated availability
      renderTimeSlots(date);
      return;
    }

    // Show loading state on button
    const bookBtn = event.target;
    const originalText = bookBtn.innerHTML;
    bookBtn.disabled = true;
    bookBtn.innerHTML = '<i class="fas fa-spinner fa-spin me-2"></i> Processing...';

    // ──────────────────────────────────────────────────────────
    // INSERT BOOKING INTO SUPABASE
    // ──────────────────────────────────────────────────────────
    const { data, error } = await supabase
      .from('bookings')
      .insert([
        {
          patient_name: name,
          phone: phone,
          email: email || null,
          age: age || null,
          appointment_date: date,
          appointment_time: time,
          service: service,
          message: message || null,
          payment_status: 'pending'
        }
      ])
      .select();

    // Restore button state
    bookBtn.disabled = false;
    bookBtn.innerHTML = originalText;

    if (error) {
      console.error('❌ Database Error:', error);
      showToast(`❌ Booking failed: ${error.message}`, "#e53e3e");
      return;
    }

    if (!data || data.length === 0) {
      showToast("❌ Booking failed. Please try again.", "#e53e3e");
      return;
    }

    // ──────────────────────────────────────────────────────────
    // SUCCESS
    // ──────────────────────────────────────────────────────────
    const bookingId = data[0].id;
    console.log('✅ Booking successful! ID:', bookingId);

    // Save booking data to sessionStorage for payment page
    sessionStorage.setItem('bookingData', JSON.stringify({
      id: bookingId,
      name: name,
      phone: phone,
      email: email,
      date: date,
      time: timeLabel,
      service: service
    }));

    // Show success message
    showToast("✅ Booking confirmed! Redirecting to payment...", "#22863a");

    // Redirect to payment after 1.5 seconds
    setTimeout(() => {
      window.location.href = RAZORPAY_PAYMENT_URL;
    }, 1500);

  } catch (error) {
    console.error('❌ Unexpected Error:', error);
    showToast("❌ An unexpected error occurred. Please try again.", "#e53e3e");
  }
}

// ════════════════════════════════════════════════════════════════
// SHOW TOAST NOTIFICATION
// ════════════════════════════════════════════════════════════════
function showToast(message, color) {
  const toast = document.getElementById("toast");
  const toastMsg = document.getElementById("toastMsg");
  toastMsg.textContent = message;
  toast.style.background = color;
  toast.classList.add("show");
  setTimeout(() => toast.classList.remove("show"), 4000);
}

// ════════════════════════════════════════════════════════════════
// INITIALIZE DATE PICKER & EVENT LISTENERS
// ════════════════════════════════════════════════════════════════
document.addEventListener('DOMContentLoaded', function() {
  const dateInput = document.getElementById("bDate");

  if (dateInput) {
    // Set minimum date to today
    dateInput.min = new Date().toISOString().split("T")[0];

    // Load slots when date changes
    dateInput.addEventListener("change", function() {
      document.getElementById("bTime").value = ""; // Clear selected time
      renderTimeSlots(this.value);
    });
  }
});

// ════════════════════════════════════════════════════════════════
// COUNTER ANIMATION (EXISTING)
// ════════════════════════════════════════════════════════════════
function animateCounters() {
  document.querySelectorAll("[data-target]").forEach((el) => {
    const target = +el.dataset.target;
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent =
        current.toLocaleString() +
        (target >= 100 ? (el.classList.contains("num") ? "" : "") : "");
      if (current >= target) clearInterval(timer);
    }, 28);
  });
}

// ════════════════════════════════════════════════════════════════
// TESTIMONIAL SLIDER (EXISTING)
// ════════════════════════════════════════════════════════════════
const testimonialSlider = document.querySelector(".testimonial-slider");
const testiTrack = document.querySelector(".testi-track");
const isAutoScrollEnabled = () => window.innerWidth >= 768;

if (testimonialSlider && testiTrack) {
  if (isAutoScrollEnabled()) testiTrack.innerHTML += testiTrack.innerHTML;
  let lastTimestamp = null;
  let offset = 0;
  const speed = 0.14;
  let paused = false;

  const animateSlider = (timestamp) => {
    if (lastTimestamp !== null && !paused && isAutoScrollEnabled()) {
      const delta = timestamp - lastTimestamp;
      offset += speed * delta;
      const resetWidth = testiTrack.scrollWidth / 2;
      if (offset >= resetWidth) offset -= resetWidth;
      testiTrack.style.transform = `translateX(${-offset}px)`;
    }
    lastTimestamp = timestamp;
    window.requestAnimationFrame(animateSlider);
  };

  testimonialSlider.addEventListener("mouseenter", () => {
    if (isAutoScrollEnabled()) paused = true;
  });
  testimonialSlider.addEventListener("mouseleave", () => {
    if (isAutoScrollEnabled()) paused = false;
  });
  window.requestAnimationFrame(animateSlider);
}

// IntersectionObserver for counters
const obs = new IntersectionObserver(
  (entries) => {
    entries.forEach((e) => {
      if (e.isIntersecting) {
        animateCounters();
        obs.disconnect();
      }
    });
  },
  { threshold: 0.3 }
);

const counterEl = document.querySelector(".counter-wrap");
if (counterEl) obs.observe(counterEl);

// AOS initialization (if needed)
if (typeof AOS !== 'undefined') {
  AOS.init({ once: true, duration: 750, easing: "ease-out-cubic" });
}

// Navbar scroll
window.addEventListener("scroll", () => {
  const nb = document.getElementById("navbar");
  if (nb) nb.classList.toggle("scrolled", window.scrollY > 60);
});
```

---

## 3. ADD CSS FOR TIME SLOTS (In `<style>` tag, after `.btn-book:hover`)

```css
/* ─── TIME SLOT STYLING ─── */
.slot-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin-bottom: 8px;
}

.time-slot {
  padding: 14px;
  border: 2px solid #e0eefe;
  border-radius: 12px;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s ease;
  background: #f9fcff;
  font-weight: 600;
  font-size: 0.85rem;
  color: var(--blue-deep);
}

.time-slot:hover:not(.booked):not(.past) {
  border-color: var(--blue-bright);
  background: #e8f4ff;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(30, 144, 255, 0.2);
}

.time-slot.selected {
  background: var(--gradient-hero);
  color: #fff;
  border-color: var(--blue-bright);
  box-shadow: 0 6px 20px rgba(21, 101, 192, 0.3);
}

.time-slot.booked {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.6;
}

.time-slot.past {
  background: #f5f5f5;
  color: #999;
  border-color: #ddd;
  cursor: not-allowed;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .slot-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .slot-grid {
    grid-template-columns: 1fr;
  }
  
  .time-slot {
    padding: 12px;
    font-size: 0.8rem;
  }
}
```

---

## 4. EXACT PLACEMENT INSTRUCTIONS

### **Step 1: Add Supabase CDN**
- Location: In `<head>` section, BEFORE closing `</head>` tag
- Add this right after Font Awesome and Bootstrap CSS links

### **Step 2: Replace JavaScript**
- Location: Inside existing `<script>` tag at bottom of file (before `</body>`)
- **REPLACE** the entire booking-related JavaScript with the code provided in Section 2
- Keep AOS initialization and navbar scroll handler code

### **Step 3: Add CSS**
- Location: Inside existing `<style>` tag in `<head>`
- Add after `.btn-book:hover` selector (around line 741)

### **Step 4: Update Credentials**
Replace these placeholders:
```javascript
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co'; // ✓ Already correct
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE'; // ← Get from Supabase dashboard
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE'; // ← Your payment link
```

---

## 5. SUPABASE TABLE SETUP (If not created yet)

Run in Supabase SQL Editor:

```sql
CREATE TABLE bookings (
  id BIGSERIAL PRIMARY KEY,
  patient_name VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  age INTEGER,
  appointment_date DATE NOT NULL,
  appointment_time VARCHAR(5) NOT NULL,
  service VARCHAR(255) NOT NULL,
  message TEXT,
  payment_status VARCHAR(50) DEFAULT 'pending',
  created_at TIMESTAMP DEFAULT now()
);

-- Create unique constraint to prevent double booking
ALTER TABLE bookings ADD CONSTRAINT unique_appointment 
UNIQUE(appointment_date, appointment_time);

-- Create index for faster queries
CREATE INDEX idx_appointment_date ON bookings(appointment_date);
```

---

## 6. SUPABASE SECURITY (RLS POLICY)

Run in Supabase SQL Editor:

```sql
-- Enable Row Level Security
ALTER TABLE bookings ENABLE ROW LEVEL SECURITY;

-- Allow public insert (no auth required)
CREATE POLICY "Allow public insert" ON bookings
  FOR INSERT WITH CHECK (true);

-- Allow public select (to check availability)
CREATE POLICY "Allow public select" ON bookings
  FOR SELECT USING (true);
```

---

## 7. VERCEL DEPLOYMENT

Add environment variables in Vercel dashboard:

```
NEXT_PUBLIC_SUPABASE_URL=https://gkzpxigyojuehhkaipci.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=YOUR_ANON_KEY_HERE
```

---

## 8. COMPLETE INDEX.HTML UPDATE

Replace the entire `<script>` section (from `<script src=...` to before `</body>`) with:

```html
<!-- SCRIPTS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.2/js/bootstrap.bundle.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>

<!-- SUPABASE CDN -->
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

<script>
// ════════════════════════════════════════════════════════════════
// SUPABASE CONFIGURATION
// ════════════════════════════════════════════════════════════════
const SUPABASE_URL = 'https://gkzpxigyojuehhkaipci.supabase.co';
const SUPABASE_ANON_KEY = 'PASTE_YOUR_ANON_KEY_HERE';
const RAZORPAY_PAYMENT_URL = 'PASTE_YOUR_RAZORPAY_LINK_HERE';

// Initialize Supabase
const { createClient } = window.supabase;
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

// ════════════════════════════════════════════════════════════════
// TIME SLOTS CONFIGURATION
// ════════════════════════════════════════════════════════════════
const TIME_SLOTS = [
  { time: "10:00", label: "10:00 AM - 11:00 AM" },
  { time: "11:00", label: "11:00 AM - 12:00 PM" },
  { time: "12:00", label: "12:00 PM - 01:00 PM" },
  { time: "13:00", label: "01:00 PM - 02:00 PM" },
  { time: "14:00", label: "02:00 PM - 03:00 PM" },
  { time: "15:00", label: "03:00 PM - 04:00 PM" },
  { time: "16:00", label: "04:00 PM - 05:00 PM" },
  { time: "17:00", label: "05:00 PM - 06:00 PM" }
];

// ════════════════════════════════════════════════════════════════
// FETCH BOOKED SLOTS FROM SUPABASE
// ════════════════════════════════════════════════════════════════
async function fetchBookedSlots(date) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('appointment_time')
      .eq('appointment_date', date);

    if (error) {
      console.error('❌ Error fetching booked slots:', error);
      return [];
    }

    return data.map(booking => booking.appointment_time);
  } catch (error) {
    console.error('❌ Unexpected error fetching slots:', error);
    return [];
  }
}

// ════════════════════════════════════════════════════════════════
// RENDER TIME SLOTS WITH AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function renderTimeSlots(date) {
  const slotContainer = document.getElementById("slotContainer");
  const selectedTime = document.getElementById("bTime").value;

  if (!date) {
    slotContainer.innerHTML = '<p style="color: #999; text-align: center; padding: 20px; grid-column: 1/-1;">Select a date to view available slots</p>';
    return;
  }

  try {
    slotContainer.innerHTML = '<p style="color: #1565c0; text-align: center; padding: 20px; grid-column: 1/-1;"><i class="fas fa-spinner fa-spin"></i> Loading slots...</p>';

    const bookedSlots = await fetchBookedSlots(date);

    const selectedDate = new Date(date);
    const today = new Date();
    today.setHours(0, 0, 0, 0);
    const isToday = selectedDate.getTime() === today.getTime();
    const currentHour = new Date().getHours();

    let slotsHtml = '';
    let availableCount = 0;

    TIME_SLOTS.forEach((slot) => {
      const hour = parseInt(slot.time.split(':')[0]);
      const isPast = isToday && hour <= currentHour;
      const isBooked = bookedSlots.includes(slot.time);
      const isSelected = selectedTime === `${slot.time}|${slot.label}`;

      let slotClass = 'time-slot';
      let slotContent = slot.label;
      let clickHandler = '';

      if (isPast) {
        slotClass += ' past';
        slotContent += ' (Past)';
      } else if (isBooked) {
        slotClass += ' booked';
        slotContent += ' ✕ BOOKED';
      } else {
        availableCount++;
        clickHandler = `onclick="selectSlot('${slot.time}', '${slot.label}')"`;
      }

      if (isSelected) {
        slotClass += ' selected';
      }

      slotsHtml += `<div class="${slotClass}" ${clickHandler}>${slotContent}</div>`;
    });

    slotContainer.innerHTML = slotsHtml;

    if (availableCount === 0) {
      const msg = isToday
        ? '<i class="fas fa-calendar-alt me-2"></i> No slots available today. Please select another date.'
        : '<i class="fas fa-check-circle me-2"></i> All slots booked for this date. Please select another date.';
      slotContainer.innerHTML = `<p style="color: #e53e3e; text-align: center; padding: 20px; grid-column: 1/-1;">${msg}</p>`;
    }
  } catch (error) {
    console.error('❌ Error rendering slots:', error);
    showToast('❌ Error loading slots. Please try again.', '#e53e3e');
  }
}

// ════════════════════════════════════════════════════════════════
// SELECT SLOT
// ════════════════════════════════════════════════════════════════
function selectSlot(time, label) {
  document.getElementById("bTime").value = `${time}|${label}`;
  renderTimeSlots(document.getElementById("bDate").value);
}

// ════════════════════════════════════════════════════════════════
// CHECK SLOT AVAILABILITY
// ════════════════════════════════════════════════════════════════
async function isSlotAvailable(date, time) {
  try {
    const { data, error } = await supabase
      .from('bookings')
      .select('id')
      .eq('appointment_date', date)
      .eq('appointment_time', time)
      .single();

    if (error && error.code === 'PGRST116') {
      return true;
    }

    if (error) {
      console.error('❌ Error checking slot:', error);
      return false;
    }

    return !data;
  } catch (error) {
    console.error('❌ Unexpected error:', error);
    return false;
  }
}

// ════════════════════════════════════════════════════════════════
// SUBMIT BOOKING
// ════════════════════════════════════════════════════════════════
async function submitBooking() {
  try {
    const name = document.getElementById("bName").value.
```

