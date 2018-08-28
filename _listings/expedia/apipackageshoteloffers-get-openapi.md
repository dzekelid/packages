---
swagger: "2.0"
x-collection-name: Expedia
x-complete: 0
info:
  title: Expedia Get Package Offers
  description: Mobile API Packages
  version: 0.0.1
host: apim.expedia.com
basePath: x/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /getpackages/v1:
    get:
      summary: Get Packages
      description: Gets packages and supports changed flights and hotels for flexible
        shopping.
      operationId: get-packages
      x-api-path-slug: getpackagesv1-get
      parameters:
      - in: query
        name: adultsPerRoom[1]
        description: How many adults will stay in the given room
      - in: query
        name: destination
        description: The userss search string
      - in: query
        name: destinationId
        description: Region ID of the origin or destination
      - in: query
        name: fromDate
        description: The date the customer wants to leave the origin
      - in: query
        name: ftla
        description: TLA (airport code or metrocode) for the origin (ftla) or destination
          (ttla)
      - in: query
        name: numberOfRooms
        description: How many hotel rooms you want
      - in: query
        name: origin
        description: The users search string
      - in: query
        name: originId
        description: Region ID of the origin or destination
      - in: query
        name: packagePIID
        description: Taken from a previous package response
      - in: query
        name: packageTripType
        description: i
      - in: query
        name: packageType
        description: Supports different views of F+H package
      - in: query
        name: pageType
        description: Only for change hotel
      - in: query
        name: searchProduct
        description: i
      - in: query
        name: toDate
        description: The date the customer wants to leave the destination
      - in: query
        name: ttla
        description: TLA (airport code or metrocode) for the origin (ftla) or destination
          (ttla)
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
  /api/packages/hotelOffers:
    get:
      summary: Get Package Offers
      description: Mobile API Packages
      operationId: packages-offers
      x-api-path-slug: apipackageshoteloffers-get
      parameters:
      - in: query
        name: checkInDate
        description: Date the traveler will be checking in to their hotel
      - in: query
        name: checkOutDate
        description: Date the traveler will be checking out of their hotel
      - in: query
        name: childTravelerAge
        description: childTravelerAge represents the age of a single child traveler
      - in: query
        name: infantSeatingInLap
        description: Set to true if infant(s) are without a reserved seat (in an adults
          lap)
      - in: query
        name: numberOfAdultTravelers
        description: 'Number of Adult Travelers (Default: 1)'
      - in: query
        name: productKey
        description: The product ID (piid) of the package you would like to get hotel
          offers for
      - in: query
        name: ratePlanCode
        description: Rate Plan Code of the selected hotel offer
      - in: query
        name: roomTypeCode
        description: Room Type Code of the selected hotel offer
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
      - Offers
      - Hotels
  /api/packages/createTrip:
    post:
      summary: Create A Trip
      description: Mobile API Packages Create Trip operation
      operationId: packages-create-trip
      x-api-path-slug: apipackagescreatetrip-post
      parameters:
      - in: formData
        name: destinationId
        description: stubbed
      - in: formData
        name: productKey
        description: The product ID (piid) of the package you would like to get hotel
          offers for
      - in: formData
        name: roomOccupants[0].childGuestAge
        description: represents the age of a single child guest staying in this room
      - in: formData
        name: roomOccupants[0].infantsInSeat
        description: Any infants in seat
      - in: formData
        name: roomOccupants[0].numberOfAdultGuests
        description: 'Number of adults staying in this room (default: 1)'
      - in: formData
        name: roomOccupants[0].seniorCount
        description: 'Number of seniors staying in this room (default: 0)'
      - in: formData
        name: tripName
        description: stubbed
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
  /api/packages/checkout:
    post:
      summary: Checkout
      description: Mobile API Packages Checkout
      operationId: packages-checkout
      x-api-path-slug: apipackagescheckout-post
      parameters:
      - in: formData
        name: city
        description: The city of the travelers billing address
      - in: formData
        name: country
        description: The 3 letter country code of the travelers billing address
      - in: formData
        name: creditCardNumber
        description: The credit card number used for this booking, if checking out
          with a new card
      - in: formData
        name: cvv
        description: The CVV of the travelers credit card used for this booking
      - in: formData
        name: doIThinkImSignedIn
        description: As a client I am checking-out with the assumption that I am signed
          in
      - in: formData
        name: expectedCardFee
        description: The expected credit card fee, as returned by the createTrip call
          in the validFormsOfPayment object for whatever credit card the user is paying
          with
      - in: formData
        name: expectedCardFeeCurrencyCode
        description: Three letter 4217 ISO currency code of the expected total price
      - in: formData
        name: expectedFareCurrencyCode
        description: Three letter 4217 ISO currency code of the expected credit card
          fee
      - in: formData
        name: expectedTotalFare
        description: The expected total price of the trip, matching exactly whatever
          the user last saw
      - in: formData
        name: expirationDateMonth
        description: The expiration date month of the credit card used for this booking
      - in: formData
        name: expirationDateYear
        description: The 4 digit expiration date year of the credit card used for
          this booking
      - in: formData
        name: flight[0].associatedFlightPassengers[0].birthDate
        description: Birth date of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].gender
        description: Gender of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].knownTravelerNumber
        description: knownTravelerNumber(PreCheckNumber) of the associated flight
          passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].passengerCategory
        description: :Passenger category of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].passportCountryCode
        description: Passport country code of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].seatPreference
        description: Seat preference of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].specialAssistanceOption
        description: Special assistance option for the associated flight passenger
          fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].title
        description: Title of the associated flight passenger fields
      - in: formData
        name: flight[0].associatedFlightPassengers[0].TSARedressNumber
        description: TSA redress number of the associated flight passenger fields
      - in: formData
        name: flight[0].mainFlightPassenger[0].email
        description: Email address of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].expediaEmailOptIn
        description: If the main flight passenger wishes to opt out for Expedia emails
          or not
      - in: formData
        name: flight[0].mainFlightPassenger[0].password
        description: Password of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].phone
        description: Phone number of the main flight passenger
      - in: formData
        name: flight[0].mainFlightPassenger[0].phoneCountryCode
        description: Country code of the phone of the main flight passenger
      - in: formData
        name: hotel[0].bedTypeId
        description: Indicates the selected bed Type
      - in: formData
        name: hotel[0].primaryContactFullName
        description: Full name of the person who will be checking in
      - in: formData
        name: nameOnCard
        description: The card holders name
      - in: formData
        name: omniturePartnerId
        description: Omniture partner identification string
      - in: formData
        name: postalCode
        description: The postal code of the travelers billing address
      - in: formData
        name: sendEmailConfirmation
        description: Used to check if confirmation email needs to be sent or not
      - in: formData
        name: state
        description: The state (or province) of the travelers billing address
      - in: formData
        name: storeCreditCardInUserProfile
        description: Indicates whether to save the credit card information as a stored
          credit card in the user profile
      - in: formData
        name: storedCreditCardId
        description: The GUID for the stored credit card information to be used for
          payment
      - in: formData
        name: streetAddress
        description: The street part of the credit card owners billing address
      - in: formData
        name: streetAddress2
        description: Apartment or suite number of the travelers billing address
      - in: formData
        name: tealeafTransactionId
        description: The unique transaction ID used in TeaLeaf PSR tracking
      - in: formData
        name: tripId
        description: The trip ID of an existing trip, from /api/packages/createTrip
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
  /api/m/trip/coupon:
    post:
      summary: Apply Coupon
      description: Mobile API Packages Apply Coupon
      operationId: packages-apply-coupon
      x-api-path-slug: apimtripcoupon-post
      parameters:
      - in: formData
        name: coupon.code
        description: Coupon Code
      - in: formData
        name: coupon.instanceId
        description: Instance ID
      - in: formData
        name: coupon.name
        description: Coupon Name
      - in: formData
        name: tripId
        description: The tripId we are going to apply the coupon to
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Coupons
      - Airlines
  /api/m/trip/remove/coupon:
    post:
      summary: Remove Coupon
      description: Mobile API Packages Remove Coupon
      operationId: packages-remove-coupon
      x-api-path-slug: apimtripremovecoupon-post
      parameters:
      - in: formData
        name: tripId
        description: The tripId we are going to apply the coupon to
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Airports
      - Airplanes
      - Coupons
      - Airlines
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---