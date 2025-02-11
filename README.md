```
.
├── README.md
├── scripts                                            Contains IaC-related scripts
├── stacks                                             Contains all terraform deployments
│   ├── aws                                            AWS MG
│   │   └── account-1
│   │       └── region-1
│   │           └── backups
│   │               └── s3
│   └── azure                                          Azure MG - Overall
│       ├── global                                     Contains all resources, configurations, etc that does not live in a subscription
│       │   ├── iam
│       │   ├── mg
│       │   ├── policies
│       │   └── subscriptions
│       ├── platform                                   Azure MG - Platform
│       │   ├── connectivity                           Azure MG - Connectivity
│       │   │   ├── bastion
│       │   │   │   ├── network
│       │   │   │   ├── rg
│       │   │   │   ├── service
│       │   │   │   └── storage
│       │   │   ├── core-network                       Stack (Solution) #1
│       │   │   │   ├── ecr                            - Unit #1
│       │   │   │   │   ├── prd-centralus               - Deployment #1 (Environment + Region)
│       │   │   │   │   ├── prd-eastus2                 - Deployment #2 (Environment + Region)
│       │   │   │   │   ├── tst-centralus               - Deployment #3 (Environment + Region)
│       │   │   │   │   └── tst-eastus2                 - Deployment #4 (Environment + Region)
│       │   │   │   ├── ecr-peering                    - Unit #2
│       │   │   │   │   ├── prd-centralus               - Deployment #1 (Environment + Region)
│       │   │   │   │   ├── prd-eastus2                 - Deployment #2 (Environment + Region)
│       │   │   │   │   ├── tst-centralus               - Deployment #3 (Environment + Region)
│       │   │   │   │   └── tst-eastus2                 - Deployment #4 (Environment + Region)
│       │   │   │   ├── hub
│       │   │   │   │   ├── prd-centralus
│       │   │   │   │   ├── prd-eastus2
│       │   │   │   │   ├── tst-centralus
│       │   │   │   │   └── tst-eastus2
│       │   │   │   ├── hub-paloalto
│       │   │   │   │   ├── prd-centralus
│       │   │   │   │   ├── prd-eastus2
│       │   │   │   │   ├── tst-centralus
│       │   │   │   │   └── tst-eastus2
│       │   │   │   ├── rg
│       │   │   │   │   ├── prd-centralus
│       │   │   │   │   ├── prd-eastus2
│       │   │   │   │   ├── tst-centralus
│       │   │   │   │   └── tst-eastus2
│       │   │   │   └── vwan
│       │   │   │       ├── prd-global
│       │   │   │       └── tst-global
│       │   │   └── privatelink
│       │   │       ├── dns-resolvers
│       │   │       │   ├── prd-centralus
│       │   │       │   ├── prd-eastus2
│       │   │       │   ├── tst-centralus
│       │   │       │   └── tst-eastus2
│       │   │       ├── dns-zones
│       │   │       │   ├── prd-global
│       │   │       │   └── tst-global
│       │   │       ├── network
│       │   │       │   ├── prd-centralus
│       │   │       │   ├── prd-eastus2
│       │   │       │   ├── tst-centralus
│       │   │       │   └── tst-eastus2
│       │   │       └── rg
│       │   │           ├── prd-centralus
│       │   │           ├── prd-eastus2
│       │   │           ├── tst-centralus
│       │   │           └── tst-eastus2
│       │   └── sharedservices                         Azure MG - Shared Services
│       │       ├── gitops                             Stack (Solution) #1
│       │       │   ├── ado-managed-pools              - Nested-Stack #1 (Optional - Limit to 2 deep)
│       │       │   │   ├── service                     - Unit #1-1
│       │       │   │   ├── workers-ubuntu              - Unit #1-2
│       │       │   │   └── workers-windows             - Unit #1-3
│       │       │   ├── automation-accounts            - Nested-Stack #2 (Optional - Limit to 2 deep)
│       │       │   │   ├── service                     - Unit #2-1
│       │       │   │   ├── workers-ubuntu              - Unit #2-2
│       │       │   │   └── workers-windows             - Unit #2-3
│       │       │   ├── keyvault                       Unit #1
│       │       │   ├── network                        Unit #2
│       │       │   ├── rg                             Unit #3
│       │       │   └── storage                        Unit #4
│       │       ├── update-manager
│       │       │   ├── rg
│       │       │   └── service
│       │       └── vm-images
│       │           ├── compute-gallery
│       │           │   ├── prd-global
│       │           │   └── tst-global
│       │           ├── image-builder
│       │           └── rg
│       └── workloads
│           ├── corp
│           │   ├── cloud-shell
│           │   ├── data-analysts
│           │   ├── mdm-data
│           │   │   ├── network
│           │   │   └── rg
│           │   ├── mdm-usertools
│           │   │   ├── acr
│           │   │   ├── aks
│           │   │   ├── logic-apps
│           │   │   ├── network
│           │   │   ├── rg
│           │   │   └── storage
│           │   └── shared-apps
│           └── online
│               ├── data-shares
│               └── public-websites
└── units
    ├── unit1
    ├── unit2
    └── unit3

114 directories, 2 files
```