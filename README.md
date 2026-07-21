# Step 1: Clone project
git clone https://github.com/Datadorf-co-ltd/paphop-driver-caregiver.git

# Step 2: Install Packages
yarn install

# Step 3: Create .env file
Create `.env` file from `.env.example`.
For Supabase, set `DATABASE_URL` to the Postgres connection string from the Supabase dashboard:
`postgresql://postgres:[YOUR-PASSWORD]@db.[PROJECT-REF].supabase.co:5432/postgres?sslmode=require`

# Step 4: Run
yarn dev

# Step 5: Create docker container
docker-compose up --build

drivecare
├─ docker-compose.yml
├─ eslint.config.mjs
├─ next.config.ts
├─ package-lock.json
├─ package.json
├─ postcss.config.mjs
├─ public
│  ├─ file.svg
│  ├─ fonts
│  │  └─ Prompt
│  │     ├─ OFL.txt
│  │     ├─ Prompt-Black.ttf
│  │     ├─ Prompt-BlackItalic.ttf
│  │     ├─ Prompt-Bold.ttf
│  │     ├─ Prompt-BoldItalic.ttf
│  │     ├─ Prompt-ExtraBold.ttf
│  │     ├─ Prompt-ExtraBoldItalic.ttf
│  │     ├─ Prompt-ExtraLight.ttf
│  │     ├─ Prompt-ExtraLightItalic.ttf
│  │     ├─ Prompt-Italic.ttf
│  │     ├─ Prompt-Light.ttf
│  │     ├─ Prompt-LightItalic.ttf
│  │     ├─ Prompt-Medium.ttf
│  │     ├─ Prompt-MediumItalic.ttf
│  │     ├─ Prompt-Regular.ttf
│  │     ├─ Prompt-SemiBold.ttf
│  │     ├─ Prompt-SemiBoldItalic.ttf
│  │     ├─ Prompt-Thin.ttf
│  │     └─ Prompt-ThinItalic.ttf
│  ├─ globe.svg
│  ├─ images
│  │  ├─ avatar.jpg
│  │  ├─ logo.png
│  │  ├─ line-logo.png
│  │  ├─ line-oa.dev-qrcode.png
│  │  ├─ line-oa.public-qrcode.png
│  │  ├─ noprofile-avatar.jpg
│  │  └─ qr-lineOA.png
│  ├─ next.svg
│  ├─ vercel.svg
│  └─ window.svg
├─ README.md
├─ src
│  ├─ app
│  │  ├─ (app)
│  │  │  ├─ booking
│  │  │  │  └─ page.tsx
│  │  │  ├─ driver-dashboard
│  │  │  │  └─ page.tsx
│  │  │  ├─ driver-job
│  │  │  │  └─ page.tsx
│  │  │  ├─ edit-profile-driver
│  │  │  │  └─ page.tsx
│  │  │  ├─ edit-profile-user
│  │  │  │  └─ page.tsx
│  │  │  ├─ health-booking
│  │  │  │  └─ page.tsx
│  │  │  ├─ job-detail
│  │  │  │  └─ [id]
│  │  │  │     └─ page.tsx
│  │  │  ├─ job-detail-user
│  │  │  │  └─ page.tsx
│  │  │  ├─ layout.tsx
│  │  │  ├─ list-reserve
│  │  │  │  └─ page.tsx
│  │  │  ├─ notifications
│  │  │  │  └─ page.tsx
│  │  │  ├─ page.tsx
│  │  │  ├─ payment
│  │  │  │  └─ page.tsx
│  │  │  └─ settings
│  │  │     └─ page.tsx
│  │  ├─ admin
│  │  │  ├─ driver
│  │  │  │  └─ [driverId]
│  │  │  │     └─ page.tsx
│  │  │  ├─ job-assignment
│  │  │  │  └─ page.tsx
│  │  │  ├─ layout.tsx
│  │  │  ├─ login
│  │  │  │  └─ page.tsx
│  │  │  ├─ manager-users
│  │  │  │  └─ page.tsx
│  │  │  ├─ overview-booking
│  │  │  │  └─ page.tsx
│  │  │  ├─ page.tsx
│  │  │  ├─ report
│  │  │  │  └─ page.tsx
│  │  │  └─ verified-slip
│  │  │     └─ page.tsx
│  │  ├─ api
│  │  │  ├─ admin
│  │  │  │  ├─ admin-controller
│  │  │  │  │  ├─ delete
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ drivers
│  │  │  │  │  │  └─ [id]
│  │  │  │  │  │     ├─ route.ts
│  │  │  │  │  │     └─ verify
│  │  │  │  │  │        └─ route.ts
│  │  │  │  │  ├─ fetch-driver
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ fetch-user
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  └─ update
│  │  │  │  │     └─ route.ts
│  │  │  │  ├─ dashboard
│  │  │  │  │  └─ route.ts
│  │  │  │  ├─ job-assignment
│  │  │  │  │  ├─ assign-driver
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ get-active-driver
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  └─ get-job-null-driver
│  │  │  │  │     └─ route.ts
│  │  │  │  ├─ logout
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ me
│  │  │  │     └─ route.ts
│  │  │  ├─ auth
│  │  │  │  ├─ admin
│  │  │  │  │  └─ login
│  │  │  │  │     └─ route.ts
│  │  │  │  ├─ drivers
│  │  │  │  │  └─ register
│  │  │  │  │     └─ route.tsx
│  │  │  │  └─ users
│  │  │  │     ├─ login
│  │  │  │     │  └─ route.ts
│  │  │  │     └─ register
│  │  │  │        └─ route.ts```
│  │  │  ├─ booking
│  │  │  │  ├─ admin
│  │  │  │  │  ├─ bookings
│  │  │  │  │  │  └─ [bookingId]
│  │  │  │  │  │     ├─ log-time-line
│  │  │  │  │  │     │  └─ route.ts
│  │  │  │  │  │     ├─ route.ts
│  │  │  │  │  │     └─ status
│  │  │  │  │  │        └─ route.ts
│  │  │  │  │  ├─ get-bookings
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ get-slip
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  └─ [id]
│  │  │  │  │     └─ handle-slip
│  │  │  │  │        └─ route.ts
│  │  │  │  ├─ drivers
│  │  │  │  │  ├─ accepted-job
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ my-job
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  ├─ my-job-detail
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  └─ [id]
│  │  │  │  │     ├─ accept
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     ├─ cancel-task
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     ├─ end
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     ├─ finish
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     ├─ log-time-line
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     ├─ start
│  │  │  │  │     │  └─ route.ts
│  │  │  │  │     └─ status
│  │  │  │  │        └─ route.ts
│  │  │  │  ├─ jobs
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ users
│  │  │  │     ├─ comfirm-booking
│  │  │  │     │  └─ route.ts
│  │  │  │     ├─ my-bookings
│  │  │  │     │  └─ route.ts
│  │  │  │     ├─ payments
│  │  │  │     │  └─ route.ts
│  │  │  │     └─ [id]
│  │  │  │        ├─ cancel-booking
│  │  │  │        │  └─ route.ts
│  │  │  │        └─ detail-booking
│  │  │  │           └─ route.ts
│  │  │  ├─ driver-controller
│  │  │  │  ├─ change-status
│  │  │  │  │  └─ route.ts
│  │  │  │  ├─ driver-logout
│  │  │  │  │  └─ route.ts
│  │  │  │  ├─ edit-profile
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ upload-image
│  │  │  │     └─ route.ts
│  │  │  ├─ health-bookinng
│  │  │  │  ├─ create-health
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ get-health
│  │  │  │     └─ route.ts
│  │  │  ├─ line
│  │  │  │  └─ webhook
│  │  │  │     └─ route.ts
│  │  │  ├─ pusher
│  │  │  │  └─ auth
│  │  │  │     └─ route.ts
│  │  │  ├─ reports
│  │  │  │  ├─ admin
│  │  │  │  │  ├─ fetch-reports
│  │  │  │  │  │  └─ route.ts
│  │  │  │  │  └─ reply-report
│  │  │  │  │     └─ route.ts
│  │  │  │  ├─ drivers
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ users
│  │  │  │     └─ route.ts
│  │  │  ├─ user-controller
│  │  │  │  ├─ edit-profile
│  │  │  │  │  └─ route.ts
│  │  │  │  └─ upload-image
│  │  │  │     └─ route.ts
│  │  │  └─ users
│  │  │     └─ route.ts
│  │  ├─ favicon.ico
│  │  ├─ globals.css
│  │  ├─ layout.tsx
│  │  ├─ login
│  │  │  └─ page.tsx
│  │  ├─ register-driver
│  │  │  └─ page.tsx
│  │  └─ register-user
│  │     └─ page.tsx
│  ├─ components
│  │  ├─ admin
│  │  │  ├─ AdminPageHeader.tsx
│  │  │  ├─ AdminRouteLoader.tsx
│  │  │  ├─ AdminSidebar.tsx
│  │  │  ├─ common
│  │  │  │  ├─ ConfirmActionModal.tsx
│  │  │  │  ├─ Pagination.tsx
│  │  │  │  └─ useEscapeToClose.ts
│  │  │  ├─ dashboard
│  │  │  │  ├─ DashboardHeaderAdmin.tsx
│  │  │  │  ├─ DonutCard.tsx
│  │  │  │  ├─ MetricCard.tsx
│  │  │  │  ├─ ReportAnalyticsCard.tsx
│  │  │  │  └─ SimpleLineChart.tsx
│  │  │  ├─ job-assignment
│  │  │  │  ├─ AssignDriverModal.tsx
│  │  │  │  ├─ JobAssignmentMobileCards.tsx
│  │  │  │  └─ JobAssignmentTable.tsx
│  │  │  ├─ manager-users
│  │  │  │  ├─ AddressModal.tsx
│  │  │  │  ├─ AdminUsersTable.tsx
│  │  │  │  ├─ Avatar.tsx
│  │  │  │  ├─ ConfirmDeleteModal.tsx
│  │  │  │  ├─ EditUserModal.tsx
│  │  │  │  ├─ FilterSelect.tsx
│  │  │  │  ├─ GroupToggle.tsx
│  │  │  │  └─ StatusBadge.tsx
│  │  │  ├─ overview-booking
│  │  │  │  ├─ BookingManageModal.tsx
│  │  │  │  └─ BookingOverviewTable.tsx
│  │  │  ├─ ReplyReportModal.tsx
│  │  │  ├─ report
│  │  │  │  └─ ReportTable.tsx
│  │  │  ├─ sidebar-menu.ts
│  │  │  └─ verified-slip
│  │  │     ├─ PaymentSlipModal.tsx
│  │  │     ├─ RejectPaymentModal.tsx
│  │  │     └─ VerifiedSlipTable.tsx
│  │  ├─ Button.tsx
│  │  ├─ common
│  │  │  └─ SelectDropdown.tsx
│  │  ├─ ConsentCheckbox.tsx
│  │  ├─ driver
│  │  │  ├─ cards
│  │  │  │  ├─ JobCard.tsx
│  │  │  │  ├─ JobPassengerCard.tsx
│  │  │  │  └─ JobScheduleRouteCard.tsx
│  │  │  ├─ dashboard
│  │  │  │  ├─ DriverDashboardApproved.tsx
│  │  │  │  ├─ DriverPendingApprovalNotice.tsx
│  │  │  │  └─ DriverRejectedNotice.tsx
│  │  │  ├─ DistanceEta.tsx
│  │  │  ├─ driver-job
│  │  │  │  ├─ EmptyState.tsx
│  │  │  │  ├─ InProgressLayout.tsx
│  │  │  │  └─ UpcomingLayout.tsx
│  │  │  ├─ ExpandableText.tsx
│  │  │  ├─ job-detail
│  │  │  │  ├─ CompletedLayout
│  │  │  │  │  ├─ CompletedLayout.tsx
│  │  │  │  │  ├─ ConfirmFinishModal.tsx
│  │  │  │  │  ├─ StatusHeader.tsx
│  │  │  │  │  ├─ TimelineSection.tsx
│  │  │  │  │  └─ TotalPriceBox.tsx
│  │  │  │  ├─ InProgressLayout
│  │  │  │  │  ├─ InProgressLayout.tsx
│  │  │  │  │  ├─ JobStatusSection.tsx
│  │  │  │  │  ├─ MapSection.tsx
│  │  │  │  │  ├─ PatientInfoCard.tsx
│  │  │  │  │  ├─ ProcessNotice.tsx
│  │  │  │  │  └─ ScheduleAndRouteCard.tsx
│  │  │  │  ├─ jobStatus
│  │  │  │  │  ├─ ConfirmStatusModal.tsx
│  │  │  │  │  ├─ JobStatusCard.tsx
│  │  │  │  │  ├─ StatusActions.tsx
│  │  │  │  │  └─ StatusProgress.tsx
│  │  │  │  └─ timeline
│  │  │  │     └─ Timeline.tsx
│  │  │  ├─ map
│  │  │  │  └─ DriverMapWithActions.tsx
│  │  │  └─ Pagination.tsx
│  │  ├─ modals
│  │  │  ├─ LineNotifyModal.tsx
│  │  │  ├─ PolicyModal.tsx
│  │  │  ├─ ReportModal.tsx
│  │  │  └─ UpslipModal.tsx
│  │  ├─ navigation-menu
│  │  │  ├─ bottom-navbar.tsx
│  │  │  └─ nav-menu.ts
│  │  └─ user
│  │     └─ StatusTrackerCard.tsx
│  ├─ constants
│  │  ├─ booking-status.ts
│  │  ├─ policy
│  │  │  ├─ driver-terms.ts
│  │  │  └─ user-terms.ts
│  │  └─ reports
│  │     └─ report-types.ts
│  ├─ context
│  │  ├─ AdminContext.tsx
│  │  └─ UserContext.tsx
│  ├─ data
│  │  └─ healthTips.ts
│  ├─ lib
│  │  ├─ cloudinary.ts
│  │  ├─ db.ts
│  │  ├─ line.ts
│  │  └─ pusher.ts
│  ├─ proxy.ts
│  ├─ services
│  │  ├─ calculatePrice.ts
│  │  ├─ map
│  │  │  ├─ location.ts
│  │  │  ├─ LongdoMap.tsx
│  │  │  ├─ PlaceSearch.tsx
│  │  │  ├─ useLongdoMap.ts
│  │  │  └─ useLongdoMapDriver.ts
│  │  └─hospital
│  │     └─ get-near-find.ts
│  ├─ store
│  │  └─ notification.state.ts
│  ├─ types
│  │  ├─ admin
│  │  │  ├─ admin.ts
│  │  │  ├─ adminContextType.ts
│  │  │  ├─ booking-overview.ts
│  │  │  ├─ bookingSlip.ts
│  │  │  ├─ dashboard.ts
│  │  │  ├─ job-assignment.ts
│  │  │  ├─ manager-users.ts
│  │  │  ├─ report.ts
│  │  │  └─ sideBar.ts
│  │  ├─ auth
│  │  │  └─ line.ts
│  │  ├─ driver
│  │  │  ├─ dashboard.ts
│  │  │  ├─ job.ts
│  │  │  ├─ route.ts
│  │  │  ├─ timeline.ts
│  │  │  └─ types.ts
│  │  ├─ forms
│  │  │  ├─ auth.ts
│  │  │  └─ edit-profile.ts
│  │  ├─ map
│  │  │  ├─ geo.ts
│  │  │  ├─ longdo.ts
│  │  │  └─ search.ts
│  │  ├─ notification.ts
│  │  ├─ profile
│  │  │  ├─ base.ts
│  │  │  ├─ driver.ts
│  │  │  └─ user.ts
│  │  ├─ profile.ts
│  │  ├─ realtime
│  │  │  └─ pusher.ts
│  │  ├─ report.ts
│  │  ├─ useContextType.ts
│  │  └─ user
│  │     ├─ bookings.ts
│  │     └─ health-bookinng.ts
│  └─ utils
│     ├─ car-list.json
│     ├─ carList.ts
│     ├─ dayjs.ts
│     ├─ db-datetime.ts
│     ├─ distance.ts
│     ├─ format-datetime.ts
│     ├─ google-maps.ts
│     ├─ pagination.ts
│     ├─ past-datetime-content.ts
│     └─ report.ts
├─ tailwind.config.ts
└─ tsconfig.json

```
