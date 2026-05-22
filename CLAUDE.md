# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **Online Jewellery Shopping Web Application** for **Yash Gems & Jewelleries (P) Ltd**. The project specification is in `OnlineJwelleryShopping.md`. No code has been written yet — this is a greenfield project.

## System Roles

- **Admin/Vendor**: Manages product catalogue, processes orders, views sales reports, manages customer records.
- **Customer**: Browses/searches jewellery, adds to cart, places orders, pays via credit card, can send gifts to alternate addresses.

## Key Features to Implement

- Product search with combinatorial filters (diamond weight, type, brand, carat, gem name, quality)
- Shopping cart (add/remove products)
- User registration and login with secure passwords
- Credit card payment processing
- Order management and dispatch
- Informational pages: diamond certification, gem history/benefits
- Admin dashboard with sales reports

## Database Schema

The backend uses SQL Server. Key tables:

| Table | Purpose |
|---|---|
| `AdminLoginMst` | Admin credentials (userName PK, Password) |
| `UserRegMst` | Customer accounts (userID PK, name, address, city, state, mobile, email, DOB, password) |
| `ItemMst` | Product catalogue (Style\_Code PK, Brand\_ID, Cat\_ID, Certify\_ID, Prod\_ID, GoldType\_ID, gold/stone weights, MRP) |
| `CartList` | Shopping cart items (ID PK, Product\_Name, MRP) |
| `BrandMst` | Jewellery brands (e.g. Asmi, D'damas) |
| `CatMst` | Product categories |
| `ProdMst` | Product types |
| `GoldKrtMst` | Gold caratage (18ct, 22ct, etc.) |
| `CertifyMst` | Certification types (918, 920, etc.) |
| `DimMst` | Diamond details per item (linked to Style\_Code, quality, carat, weight, rate) |
| `DimQltyMst` | Diamond quality grades (AD, FD, VVS, etc.) |
| `DimQltySubMst` | Diamond sub-types |
| `DimInfoMst` | Diamond reference info with images |
| `StoneMst` | Stone details per item (linked to Style\_Code) |
| `StoneQltyMst` | Stone types (Ruby, Meena, etc.) |
| `JewelTypeMst` | Jewellery type classification |
| `Inquiry` | Customer inquiries/contact form submissions |

### Key Relationships
- `ItemMst.Style_Code` → FK in `DimMst` and `StoneMst` (one item can have multiple diamonds/stones)
- `ItemMst` references `BrandMst`, `CatMst`, `CertifyMst`, `ProdMst`, `GoldKrtMst` via foreign keys
- `DimMst` references `DimQltyMst` and `DimQltySubMst`

### Price Calculation (ItemMst)
`MRP = Gold_Amt + Gold_Making + Stone_Making + Other_Making`  
Where `Gold_Amt = Net_Gold × Gold_Rate` and wastage is factored in.
