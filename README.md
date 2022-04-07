mest kitchen:
    user:
        id
        fname
        lname
        email
        allergy
        status
        role : master, cook, kitchen_user
    user_role:
        id
        name
        desc
    allergy:
        id
        name
        desc

    MenuItem:
        name
        desc
        type: breakfast, lunch, dinner
        price

    Order(MenuItem):
        orderId
        quantity
        total = MenuItem.price * quantity
        recipient = User('user_id')

    

