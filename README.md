# live-pesa
# modules
# ------------------------------------------------------------------------------------------------------------------
                                     Authentication
------------------------------------------------------------------------------------------------------------------
            Register      |         Login        |        Verification         |         Password recovery        
------------------------------------------------------------------------------------------------------------------ 
# Register 
    # Normal user registration
        -Done via USSD  
            #Some Required information
                ->Phone number
                ->Password
                ->Location
                ->Security Question
        -Done via live pesa app
            -#Some Required information
                ->Phone number
                ->Password
                ->Location
                ->Security Question

    # Agents registration
        -Done via application  form / on system
            #Some required information
                * Agent basic info
                    ->Full name
                    ->Email
                    ->Phone number
                    ->Nida ID/copy ,TIN,Copy
                    ->Post adress 
                    ->Physical address

    # Merchants registration
        -Done via application  form / on system
            #Some required information
                * Agent basic info
                    ->Full name
                    ->Email
                    ->Phone number
                    ->Nida ID/copy ,TIN,Copy
                    ->Post adress 
                    ->Physical address

    # Top Adiminstrator
        -Done via simple form registration supervised by company
                # include
                    ->Main agent 
                    ->Costumer service
                    ->System adminstrator
                
                # Some Required info
                    ->Employee number
                    ->Sequrity Question
                    ->Password
-----------------------------------------------------------------------------------------------------------------
# Login
    # Normal user login
        -Done via USSD ->TARGET->User USSD Page
            # Some Reqired information
                ->Phone number
                ->Password
       -Done via Live pesa app
            # Some Reqired information
                ->Phone number
                ->Password

    # Agents login
        -Done via USSD ->TARGET->Agent USSD Page
            # Some Required information
                ->Agent number
                ->Password
        -Done via Live pesa agent app
            ->Agent number
            ->Password

     # Merchant login
        -Done via USSD ->TARGET->Merchant USSD Page
            # Some Required information
                ->Merchant number
                ->Password
        -Done via Live pesa merchant app
            ->Merchant number
            ->Password

    # Top administrator login
        -Done via system login page
            # Some required infomartion
                ->Employee number
                ->Password
------------------------------------------------------------------------------------------------------------------
# Verification
    # Users -> Live pesa App registration
        #Some reqired information
            ->Verification code
    
     # Agents -> Live pesa Agents App registration
        #Some reqired information
            ->Verification code

     # Merchant -> Live pesa Merchant App registration
        #Some reqired information
            ->Verification code
------------------------------------------------------------------------------------------------------------------
# Password recovery
    # Normal Users password recovery
        -Done via USSD
        # Some required information
            ->Phone number
            ->Security question
            ->NIDA Number

    # Agents Password recovery
         -Done via USSD
        # Some required information
            ->Agent number
            ->Security question
            ->NIDA Number
    
    # Merchant Password recovery
         -Done via USSD
        # Some required information
            ->Merchant number
            ->Security question
            ->NIDA Number


    # Top adiminstrator
        -Done via system password recovery option
        # Some required information
            ->Employee number
            ->Sequrity question
------------------------------------------------------------------------------------------------------------------
##### [SUGGESTION For admins who have full access to transaction, authentication can be done through biometric auth system to ensure Bank level security.]
------------------------------------------------------------------------------------------------------------------


------------------------------------------------------------------------------------------------------------------
                                                SYSTEM USERS
------------------------------------------------------------------------------------------------------------------
                                              ACCESS AND ROLES
------------------------------------------------------------------------------------------------------------------
    Normal users     |          Agents     |          Merchants             |            Top Adminstrators
------------------------------------------------------------------------------------------------------------------
# Normal users
    # Transaction 
        -> Paid Transaction
            -Send money
            -Withdraw Money
            -Balance
    # Account information
        ->Only one account


# Agents
    # Transaction
        ->Free transaction
            -Sending money to another agent
            -Send Money to normal user
            -Balance
    # Account information
        -Only one account
    # Code withdraw
    # Access to commision
    # Access to Agents Bonus
# Merchants
     # Transaction 
        -> Paid Transaction
            -Send money [Free]
            -Withdraw Money[Commission]
            -Balance[free]
    # Account information
        ->Only one account
# Top adiminstrators
    # Main Agents
        # Transaction 
            # Free transaction
                ->Free deposits to  small agents
                ->Free withdraw from small agents
        # Account information 
        # Access to basic information of all small agents
        # Access to block agent in case of any violations

    # Customer services
        # Partial access to all transaction made /only view
        # Full access to all users basic information
        # Access to Block transction
    # Top system admin #user management side
            ->Full access to users management
            ->Full access to agents management
            ->Full access to system adiminstrators management
     # Top system admin # Transaction management side
            -> Full access to all transaction
                ->Transaction reversal
                ->Transaction block
------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------
# USERS  MODULE
# Normal user module 
    #FOR USSD
    ->Send Money ->Same network                           ->Enter number -> Enter amount ->  verify name and amount ->Enter password  ->SUBMIT ->CLOSE
                 ->Send to other network -> M-Pesa        ->Enter vodacom number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                         -> TigoPESA      ->Enter tigo number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                         -> Airtel money  ->Enter airtel number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                         -> Eazy Pesa     ->Enter zantel number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                         -> T-pesa        ->Enter ttcl number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                         -> Halo pesa     ->Enter halotel number -> Enter amount  -> verify name and amount  ->Enter password  ->SUBMIT ->CLOSE

                 ->Send to Bank -> CRDB                   ->Enter card number -> Enter amount  ->  verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                -> NMB                    ->Enter card number -> Enter amount  ->  verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                -> NBC                    ->Enter card number -> Enter amount  ->  verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                -> UCB                    ->Enter card number -> Enter amount  ->  verify name and amount  ->Enter password  ->SUBMIT ->CLOSE
                                -> EXIM                   ->Enter card number -> Enter amount  ->  verify name and amount  ->Enter password  ->SUBMIT ->CLOSE

                 ->Send as Gift card
