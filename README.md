# Sterling Row Barbers

A responsive website for Sterling Row, a fictional neighbourhood barbershop in De Waterkant, Cape Town. It is a static site built with HTML, CSS, and JavaScript. There is no build step and no backend.

Visitors can browse services, meet the barbers, find the shop, and book a chair in the browser.

The live site is at [https://sterling-row-barbers.netlify.app/](https://sterling-row-barbers.netlify.app/).

## Pages

- **Home** shows the shop intro, a short service list, a photo gallery, and a first-visit offer.
- **Services** lists the full board, with prices and times.
- **About** introduces the three barbers.
- **Contact** has the address, hours, a message form, and a map.
- **Booking** lets a visitor choose a service, barber, date, and time, then save the appointment to their calendar.
- **Terms** and **Privacy** cover the shop’s booking rules and how details are handled.

## Run it locally

Open `index.html` in a browser, or serve the folder so links and assets load the same way they will online:

```bash
python -m http.server 8899
```

Then visit [http://127.0.0.1:8899/](http://127.0.0.1:8899/).

## Booking

Appointments are confirmed in the browser. Nothing is sent to a server. The form builds a calendar event from the visitor’s choices, with a Google Calendar link and a downloadable `.ics` file for Apple Calendar and Outlook.

The shop is open Monday to Friday, 08:00–18:00, and Saturday, 08:00–16:00. Sunday is closed, so a Sunday date is rejected. Times are every 30 minutes, and a booking must finish before closing.

A service can be preselected with `?service=` (for example `booking.html?service=fade`). The first-visit code `FIRSTCUT` can be passed with `?promo=FIRSTCUT`.

## Shop details

Sterling Row is fictional. The details used on the site are:

- 14 Sterling Row, De Waterkant, Cape Town 8001
- 021 555 0148
- hello@sterlingrow.co.za
- Barbers: Elias Marlow, Jonah Adeyemi, and Sibusiso Nkosi
