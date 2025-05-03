# artisan-craftman-project

## Terms definition

* **Craftsmanship** :
**Craftsmanship** refers to the set of manual and traditional activities aimed at creating useful or decorative objects. It encompasses various trades such as carpentry, pottery, sewing, jewelry making, and many others. Artisans often use ancestral techniques and natural materials to produce unique pieces or small batches.

* **Craftsman or Artisan** :
A **craftsman** is a person who practices a manual and traditional trade. They master specific techniques to manufacture, repair, or restore objects. Craftsmen are often recognized for their skill, creativity, and attention to detail.

# Classes or entities definiotion

### Enumerations

1. **UserAccountStatus**

   * **Description**: Represents the various states of a user account.
   * **Role**: Manages the account lifecycle (active, inactive, suspended, pending approval).

2. **WorkshopStatus**

   * **Description**: Indicates the operational state of a workshop.
   * **Role**: Tracks whether a workshop is open, temporarily, or permanently closed.

3. **CraftworkStatus**

   * **Description**: Defines the status of a craftwork item (available, sold, made-to-order, archived).
   * **Role**: Manages the availability and sales lifecycle of craftworks.

4. **ReviewStatus**

   * **Description**: Represents the state of a customer review (pending, approved, rejected).
   * **Role**: Controls the moderation process of customer feedback.

5. **PricingType**

   * **Description**: Types of pricing for a service (hourly, flat-rate, quote-based).
   * **Role**: Defines the billing method for provided services.

6. **ServiceStatus**

   * **Description**: Status of a service (active, inactive).
   * **Role**: Indicates whether a service is currently being offered.

7. **ServiceRequestStatus**

   * **Description**: States of a service request (new, in progress, accepted, rejected, etc.).
   * **Role**: Tracks the lifecycle of a request from submission to completion.

8. **QuoteStatus**

   * **Description**: Status of a quote (issued, accepted, rejected, expired).
   * **Role**: Manages the negotiation process through quote tracking.

9. **OrderStatus**

   * **Description**: States of an order (cart, paid, shipped, delivered, etc.).
   * **Role**: Tracks order progress throughout the purchasing process.

10. **MediaType**

    * **Description**: Types of media files (image, video, audio, document, etc.).
    * **Role**: Classifies media linked to entities such as artworks, services, or certifications.

11. **PromotionStatus**

    * **Description**: Status of a promotion (active, inactive, expired, scheduled).
    * **Role**: Manages the lifecycle of product or service promotions.

12. **PaymentMethod**

    * **Description**: Available payment methods (credit card, PayPal, cash, etc.).
    * **Role**: Identifies options for transaction payments.

13. **PaymentStatus**

    * **Description**: Payment status (pending, successful, failed, refunded, etc.).
    * **Role**: Tracks the state of financial transactions.

14. **MobileOperator**

    * **Description**: Mobile payment providers (Orange Money, MTN MoMo, etc.).
    * **Role**: Specifies the provider used for mobile transactions.

15. **ReferralStatus**

    * **Description**: Status of a referral (pending, active, expired, cancelled).
    * **Role**: Manages referral relationships between users.

16. **RelayPointType**

    * **Description**: Types of relay points (partner store, locker, post office).
    * **Role**: Classifies delivery pickup/drop-off locations.

17. **DeliveryStatus**

    * **Description**: Delivery statuses (pending, shipped, delivered, failed, etc.).
    * **Role**: Tracks delivery progress.

18. **TransportType**

    * **Description**: Types of transportation used (bike, scooter, car, van).
    * **Role**: Identifies the vehicle used by a delivery agent.

19. **DeliveryType**

    * **Description**: Delivery types (standard, redelivery, return).
    * **Role**: Specifies the context of a delivery.

20. **ReturnStatus**

    * **Description**: Return status (requested, received, refunded, rejected, etc.).
    * **Role**: Manages the product return lifecycle.

21. **ComplaintType**

    * **Description**: Types of complaints (defective product, delay, poor service, etc.).
    * **Role**: Categorizes customer complaints for proper resolution.

---

### Classes

1. **GeoAddress**

   * **Description**: Represents a geographic address with coordinates, neighborhood, city, etc.
   * **Role**: Provides a structure to store and manage address information for clients, workshops, deliveries, etc.

2. **Media**

   * **Description**: Manages multimedia files (images, videos, documents) with type, URL, and size.
   * **Role**: Links media content to artworks, artisans, services, quotes, etc., for documentation or promotion.

3. **Occupation**

   * **Description**: Represents a trade or specialty practiced by an artisan.
   * **Role**: Categorizes artisan skills and associates them with services or products.

4. **Certification**

   * **Description**: Stores information about an artisan's certification (name, organization, dates).
   * **Role**: Validates qualifications and enhances artisan credibility.

5. **Availability**

   * **Description**: Manages an artisan’s availability or unavailability periods.
   * **Role**: Schedules interventions or services accordingly.

6. **Promotion**

   * **Description**: Represents a promotional offer with code, discount, and validity period.
   * **Role**: Applies discounts to artworks or services to boost sales.

7. **Person**

   * **Description**: Abstract class for human entities (name, email, address, etc.).
   * **Role**: Provides a base for derived classes such as Client and Artisan.

8. **UserAccount**

   * **Description**: Manages authentication information and user roles.
   * **Role**: Secures system access and assigns roles (admin, client, artisan).

9. **Role**

   * **Description**: Defines a user role with name and description.
   * **Role**: Manages permissions and responsibilities within the system.

10. **Client**

    * **Description**: Specialized Person class for clients, with order and review history.
    * **Role**: Represents buyers placing orders or requesting services.

11. **Artisan**

    * **Description**: Specialized Person class for artisans, with specialties, workshops, and artworks.
    * **Role**: Manages creators and service providers.

12. **Workshop**

    * **Description**: Represents a physical location where an artisan works.
    * **Role**: Organizes artisan activities and serves as a reference for services/products.

13. **Craftwork**

    * **Description**: Represents an artisan product with price, stock, and status.
    * **Role**: Manages sale items with potential for promotions and reviews.

14. **Review**

    * **Description**: Stores client feedback with rating and comments.
    * **Role**: Builds trust and provides quality feedback.

15. **OfferedService**

    * **Description**: Represents a service provided by an artisan, with pricing and type.
    * **Role**: Manages available services and their related requests.

16. **ServiceRequest**

    * **Description**: Represents a service request by a client, with status and quote.
    * **Role**: Facilitates communication between clients and artisans.

17. **Quote**

    * **Description**: Represents a quote issued for a service request.
    * **Role**: Formalizes financial proposals before service approval.

18. **Order**

    * **Description**: Manages a client order with items, status, payment, and delivery info.
    * **Role**: Central hub of the purchase process from creation to delivery.

19. **OrderLine**

    * **Description**: Represents a specific item in an order.
    * **Role**: Details products included in the order.

20. **PurchaseOrder**

    * **Description**: Official document associated with an order.
    * **Role**: Serves as proof of purchase agreement.

21. **Invoice**

    * **Description**: Represents an invoice issued for an order.
    * **Role**: Handles billing and payment tracking.

22. **Payment**

    * **Description**: Manages payment details, including method and status.
    * **Role**: Tracks financial transactions and results.

23. **Transaction**

    * **Description**: Represents a specific payment attempt.
    * **Role**: Logs payment attempts and outcomes.

24. **ReferralCampaign**

    * **Description**: Manages a referral campaign with conditions and rewards.
    * **Role**: Encourages new user acquisition through incentives.

25. **Referral**

    * **Description**: Represents a referral relationship between two users.
    * **Role**: Manages codes and credits between sponsors and referees.

26. **RelayPoint**

    * **Description**: Represents a delivery drop-off/pick-up location.
    * **Role**: Supports delivery logistics via intermediary points.

27. **DeliveryAgent**

    * **Description**: Represents a person responsible for deliveries.
    * **Role**: Manages assignment of deliveries.

28. **Delivery**

    * **Description**: Manages the delivery process, including status and agents.
    * **Role**: Tracks delivery from dispatch to reception.

29. **Parcel**

    * **Description**: Represents a physical package with dimensions and contents.
    * **Role**: Manages shipment units in a delivery.

30. **ParcelItem**

    * **Description**: Represents a specific item within a parcel.
    * **Role**: Links order lines to shipped parcels.

31. **Return**

    * **Description**: Manages return requests, including status and refund.
    * **Role**: Handles the return lifecycle.

32. **ReturnItem**

    * **Description**: Represents a specific returned item.
    * **Role**: Details the products included in a return.

33. **Refund**

    * **Description**: Manages refunds for returns or payments.
    * **Role**: Finalizes refund processes for clients.

34. **Complaint**

    * **Description**: Represents a client complaint with details and resolution.
    * **Role**: Handles disputes or issues raised by clients.

35. **Notification**

    * **Description**: Represents a message sent to a user, with read status.
    * **Role**: Communicates alerts and updates to users.

36. **ClientDeliveryAddress**

    * **Description**: Stores a specific delivery address for a client.
    * **Role**: Allows clients to manage multiple delivery addresses.

---














