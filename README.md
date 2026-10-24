# vetcare

```mermaid
graph LR
    subgraph VetCare [VetCare Veterinary Management System]
        %% Authentication
        L([Register Account / Sign Up])
        LI([Login / Logout])
        FP([Forgot Password])

        %% User Management (Admin)
        AU([Add New User & Assign Role])
        EU([Edit User Details & Permissions])
        DU([Delete User Account])
        VU([View Registered Users List])

        %% Dashboard & Profile Settings
        VD([View Admin Dashboard Metrics])
        EAP([Edit Admin Profile & Settings])
        MCI([Manage Clinic Information])
        MOH([Set Operating Hours & Alerts])
        CP([Change Password])

        %% Pet Profile & Details
        AP([Add New Pet Profile & Photo])
        VP([View All Pets by Species - Dog, Cat, Rabbit, Bird])
        SP([Search Pet by Name, ID, or Owner])
        UPD([Update Pet Details & Photo])

        %% Clinical & Health Records
        VMR([View Medical History Logs])
        UMR([Add / Update Medical Record])
        VVR([View Vaccination Logs])
        UVR([Update Vaccination Record])

        %% Appointment Management & Status Filters
        BA([Book New Appointment])
        VPB([View Pending Appointment Requests])
        VCA([View Confirmed Appointments])
        VCM([View Completed Visits])
        VCN([View Cancelled Visits])
        RA([Reschedule Appointment])

        %% Messaging & Communication
        SM([Send Message / Chat])
        RM([Receive Client Messages in Inbox])

        %% Reports & Analytics (Admin)
        VAR([View Appointment Reports & Peak Times])
        VPR([View Pet Reports & Demographics])
        VUR([View User Reports & System Logs])
        VVR2([View Veterinarian Performance Reports])
        VSR([View Service Revenue Reports])
    end

    %% Admin Connections (Full System Access)
    Admin --- LI & FP & AU & EU & DU & VU & VD & EAP & MCI & MOH & CP & AP & VP & SP & UPD & VMR & UMR & VVR & UVR & VPB & VCA & VCM & VCN & RA & RM & VAR & VPR & VUR & VVR2 & VSR

    %% Veterinarian Connections (Clinical Operations)
    Vet --- LI & FP & VP & SP & VMR & UMR & VVR & UVR & VCA & VCM & RM

    %% Pet Owner Connections (Client Actions)
    Owner --- L & LI & FP & AP & VP & SP & UPD & VMR & VVR & BA & RA & SM
'''
