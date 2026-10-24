# vetcare

```mermaid
graph LR
    %% Left Actors
    Admin["👤 Admin"]
    Vet["👤 Veterinarian"]

    subgraph VetCare [VetCare Management System]
        %% Authentication & Profiles
        SU([Sign Up / Register])
        LI([Login / Logout])
        FP([Forgot Password])

        %% Admin & User Operations
        UM([User Management])
        AU([Add User])
        EU([Edit User Details])
        DU([Delete User Account])
        RU([View Registered Users])

        %% Dashboard & Profile Settings
        VD([View Dashboard Metrics])
        APS([Admin Profile Settings])
        CI([Manage Clinic Info])
        OH([Set Operating Hours])
        CP([Change Password])

        %% Pet Profile & Categorization
        AP([Add Pet Record])
        SP([Search Pet Record])
        VP([View All Pets])
        VDC([View Pets by Category - Dog, Cat, Rabbit, Bird])

        %% Health & Clinical Records
        MH([View Medical History])
        AMR([Add/Update Medical Record])
        VL([View Vaccination Logs])
        UVR([Update Vaccination Record])

        %% Appointment Management & Status Filters
        BA([Book Appointment])
        PA([View Pending Requests])
        CA([View Confirmed Visits])
        CV([View Completed Visits])
        CX([View Cancelled Visits])
        RA([Reschedule Appointment])

        %% Communication
        MSG([Send / Receive Messages])

        %% Analytics & Reports
        AR([Appointment Reports])
        PR([Pet Demographics Reports])
        UR([User Activity Reports])
        VR([Veterinarian Reports])
        SR([Service Revenue Reports])
    end

    %% Right Actor
    Owner["👤 Pet Owner"]

    %% Admin Connections (Left)
    Admin --- LI & FP & UM & AU & EU & DU & RU & VD & APS & CI & OH & CP & AP & SP & VP & VDC & MH & AMR & VL & UVR & PA & CA & CV & CX & RA & MSG & AR & PR & UR & VR & SR

    %% Vet Connections (Left)
    Vet --- LI & FP & SP & VP & VDC & MH & AMR & VL & UVR & CA & CV & MSG

    %% Pet Owner Connections (Right)
    Owner --- SU & LI & FP & AP & SP & VP & VDC & MH & VL & BA & RA & MSG
