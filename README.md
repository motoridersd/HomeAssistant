# HomeAssistant

A collection of HomeAssistant Automations and other things I use

## Flight Notifications

This automation listens for Flightradar24 integration events and then uses the Chime TTS add on to announce the flight Airline and Number (spelled out, ie 466 becomes Four Six Six). It also sends a notification to my phone and provides three parameters from the flightradar24 event.

The Condition limits the flights to what I care about, in this case it's those flying from overseas into SAN, and they only come from MUC, LHR, CDG and NRT. This can be changed to use any condition available in the event. Replace 'airport_origin_code_iata' with any other value and then adjust the conditions accordingly.

The information in the notification also uses the values in the Flightradar24 event, which are the same as the sensor.

    flight_number: UA790
    callsign: UAL790
    aircraft_registration: N27520
    aircraft_photo_small: https://cdn.jetphotos.com/200/5/1175525_1703147040_tb.jpg?v=0
    aircraft_photo_medium: https://cdn.jetphotos.com/400/5/1175525_1703147040.jpg?v=0
    aircraft_photo_large: https://cdn.jetphotos.com/640cb/5/1175525_1703147040.jpg?v=0
    aircraft_model: Boeing 737 MAX 9
    aircraft_code: B39M
    airline: United Airlines
    airline_short: United Airlines
    airline_iata: UA
    airline_icao: UAL
    airport_origin_name: New York Newark Liberty International Airport
    airport_origin_code_iata: EWR
    airport_origin_code_icao: KEWR
    airport_origin_country_name: United States
    airport_origin_country_code: US
    airport_origin_city: New York
    airport_destination_name: San Diego International Airport
    airport_destination_code_iata: SAN
    airport_destination_code_icao: KSAN
    airport_destination_country_name: United States
    airport_destination_country_code: US
    airport_destination_city: San Diego
    time_scheduled_departure: 1713090600
    time_scheduled_arrival: 1713112320
    time_real_departure: 1713091487
    time_real_arrival: null
    time_estimated_departure: null
    time_estimated_arrival: 1713110988
    latitude: 32.6771
    longitude: -116.9568
    altitude: 4200
    heading: 286
    ground_speed: 185
    squawk: ""
    vertical_speed: -1152
    tracked_by_device: FlightRadar24
