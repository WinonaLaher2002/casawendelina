# Casa Wendelina Boutique Hotel – Booking System

A single-page hotel reservation system for **Casa Wendelina Boutique Hotel**, built with plain HTML, CSS and JavaScript. No frameworks, no build step, no backend required to try it out.

## Features

### Guest side
- **Room search** by check-in date, check-out date and number of persons
- **Live availability** per room type, showing rooms left for the chosen dates
- Rooms that are sold out or too small for the group are disabled automatically
- **Price breakdown** per night: number of nights, persons per night, rate × nights, plus 12% VAT
- **Guest details form**: name, mobile number, mode of payment, arrival time and special requests
- **Booking confirmation** with a unique reference code (e.g. `CW-X7K2PQ`)
- **My Booking** lookup and cancellation using the booking reference and mobile number

### Staff side
- Passcode-protected dashboard
- Stats: upcoming bookings, arriving today, in-house guests and booked revenue
- Full bookings table (guest, mobile, room, persons, nights, total, payment mode, status)
- Cancel any booking

## Rooms (sample data)

| Room | Rate / night | Max guests | Rooms available |
|------|--------------|-----------|-----------------|
| Olive Queen | ₱3,800 | 2 | 6 |
| Deluxe King | ₱5,200 | 3 | 5 |
| Casa Family | ₱6,900 | 4 | 3 |
| Wendelina Suite | ₱9,800 | 3 | 2 |

Example: Casa Family for 4 persons over 2 nights = ₱6,900 × 2 = ₱13,800 + 12% VAT.

## Modes of payment (recorded only)
Cash (pay at hotel), GCash, Maya, Bank transfer, Credit / debit card (at hotel).
The system **records** the chosen method but does not process payments.

## Getting started

1. Clone or download this repository.
2. Open `casa-wendelina-booking.html` in any modern browser.

To host it online, deploy the file with GitHub Pages, Vercel or Netlify. Rename it to `index.html` if the host expects that.

## Configuration

Everything is configured at the top of the `<script>` section in `casa-wendelina-booking.html`:

- `ROOMS` – room names, rates, capacity, number of rooms and amenities
- `VAT` – tax rate (default `0.12`)
- `PASS` – staff passcode (default `wendelina`; **change it before going live**)

## Important limitations

- Bookings are saved in the **browser's localStorage**, so they are visible only on the device and browser where they were made. This is a front-end demo, not a shared live system.
- The staff passcode is stored in the page source and is **not real security**.
- No payment processing and no email or SMS notifications.

## Roadmap

- [ ] Backend and database (Supabase, Firebase or Node + PostgreSQL) so all bookings are shared
- [ ] Real staff authentication
- [ ] Payment gateway (GCash, Maya, cards)
- [ ] SMS confirmations
- [ ] Printable guest registration slip
- [ ] Room photos and calendar view for staff

## Tech stack

HTML5 · CSS3 · Vanilla JavaScript · Google Fonts (Cormorant Garamond, Jost)

## License

Add a license of your choice (for example MIT) before publishing.
