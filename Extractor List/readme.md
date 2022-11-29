| SAP   Extractor       | Full Name                                                   | Description                                     |  Full / Delta | Fact / Dim | Project |
|-----------------------|-------------------------------------------------------------|-------------------------------------------------|:-------------:|:----------:|---------|
| 0AC_DOC_TYP_TEXT      | Document Type - 0AC_DOC_TYP_TEXT                            | Document Type                                   | Full          |     Dim    | FI      |
| 0ASSET_AFAB_ATTR      | Depreciation Area Real or Derived - 0ASSET_AFAB_ATTR        | Depreciation Area Real or Derived               | Delta         |     Dim    | FI      |
| 0ASSET_AFAB_TEXT      | Depreciation area real or derived text - 0ASSET_AFAB_TEXT   | Depreciation area real or derived text          | Full          |     Dim    | FI      |
| 0ASSET_ATTR           | Asset Subnumber with Description - 0ASSET_ATTR              | Asset Subnumber with Description                | Full          |     Dim    | FI      |
| 0ASSET_ATTR_TEXT      | Asset Subnumber with Description Text - 0ASSET_ATTR_TEXT    | Asset Subnumber with Description Text           | Full          |     Dim    | FI      |
| 0ASSET_CLAS_TEXT      | Asset Class Master - 0ASSET_CLAS_TEXT                       | Asset Class Master                              | Full          |     Dim    | FI      |
| 0ASSET_MAIN_TEXT      | Asset Class Text - 0ASSET_MAIN_TEXT                         | Asset Class Text                                | Full          |     Dim    | FI      |
| 0CHRT_ACCTS_ATTR      | Chart of Accounts Master - 0CHRT_ACCTS_ATTR                 | Chart of Accounts Master                        | Full          |     Dim    | FI      |
| 0CHRT_ACCTS_TEXT      | Chart of Accounts Text - 0CHRT_ACCTS_TEXT                   | Chart of Accounts Text                          | Full          |     Dim    | FI      |
| 0CO_AREA_ATTR         | Controlling Area Master - 0CO_AREA_ATTR                     | Controlling Area Master                         | Full          |     Dim    | FI, IM  |
| 0CO_AREA_TEXT         | Controlling Area Text - 0CO_AREA_TEXT                       | Controlling Area Text                           | Full          |     Dim    | FI, IM  |
| 0COMP_CODE_ATTR       | Company Code Master - 0COMP_CODE_ATTR                       | Company Code Master                             | Full          |     Dim    | FI, IM  |
| 0COMP_CODE_TEXT       | Company Code Text - 0COMP_CODE_TEXT                         | Company Code Text                               | Full          |     Dim    | FI, IM  |
| 0COSTCENTER_ATTR      | Cost Center Master - 0COSTCENTER_ATTR                       | Cost Center Master                              | Full          |     Dim    | FI, IM  |
| 0COSTCENTER_TEXT      | Cost Center Text - 0COSTCENTER_TEXT                         | Cost Center Text                                | Delta         |     Dim    | FI, IM  |
| 0COSTELMNT_ATTR       | Cost Element Master - 0COSTELMNT_ATTR                       | Cost Element Master                             | Delta         |     Dim    | FI      |
| 0COSTELMNT_TEXT       | Cost Element Text - 0COSTELMNT_TEXT                         | Cost Element Text                               | Delta         |     Dim    | FI      |
| 0CUSTOMER_ATTR        | Customer Master - 0CUSTOMER_ATTR                            | Customer Master                                 | Delta         |     Dim    | ALL     |
| 0CUSTOMER_TEXT        | Customer Text - 0CUSTOMER_TEXT                              | Customer Text                                   | Delta         |     Dim    | ALL     |
| 0DEPRARTYPE_TEXT      | Standardization of Deprec. Area  -   0DEPRARTYPE_TEXT       | Standardization of Deprec. Area                 | Full          |     Dim    | FI      |
| 0EMPLOYEE_ATTR        | Employee Master - 0EMPLOYEE_ATTR                            | Employee Master                                 | Full          |     Dim    | O2C     |
| 0FI_AA_11             | Asset Accounting: Transactions - 0FI_AA_11                  | Asset Accounting: Transactions                  | Delta         |    Fact    | FI      |
| 0FI_AA_12             | Asset Accounting: Posted Depreciations - 0FI_AA_12          | Asset Accounting: Posted Depreciations          | Delta         |    Fact    | FI      |
| 0FI_AP_4              | Vendors: Line Items with Delta Extraction - 0FI_AP_4        | Vendors: Line Items with Delta Extraction       | Delta         |    Fact    | FI      |
| 0FI_AR_4              | Accounts Receivable - 0FI_AR_4                              | Accounts Receivable                             | Delta         |    Fact    | FI, O2C |
| 0FI_GL_10             | General Ledger: Leading Ledger Balances - 0FI_GL_10         | General Ledger: Leading Ledger Balances         | Delta         |    Fact    | FI      |
| 0FI_GL_14             | General Ledger (New): Line Items Leading Ledger - 0FI_GL_14 | General Ledger (New): Line Items Leading Ledger | Delta         |    Fact    | FI      |
| 0GL_ACCOUNT_ATTR      | G/L Account Master - 0GL_ACCOUNT_ATTR                       | G/L Account Master                              | Delta         |     Dim    | FI, IM  |
| 0GL_ACCOUNT_TEXT      | G/L Account Text  -   0GL_ACCOUNT_TEXT                      | G/L Account Text                                | Full          |     Dim    | FI, IM  |
| 0MAT_PLANT_ATTR       | Material Number with Plant - 0MAT_PLANT_ATTR                | Material Number with Plant                      | Delta         |     Dim    | IM      |
| 0MATERIAL_ATTR        | Material Master - 0MATERIAL_ATTR                            | Material Master                                 | Delta         |     Dim    | FI, IM  |
| 0MATERIAL_TEXT        | Material Text - 0MATERIAL_TEXT                              | Material Text                                   | Delta         |     Dim    | FI, IM  |
| 0MATL_CAT_TEXT        | Material Category - 0MATL_CAT_TEXT                          | Material Category                               | Full          |     Dim    | FI, IM  |
| 0MATL_GROUP_TEXT      | Material Group - 0MATL_GROUP_TEXT                           | Material Group                                  | Full          |     Dim    | FI, IM  |
| 0MATL_TYPE_TEXT       | Material Type - 0MATL_TYPE_TEXT                             | Material Type                                   | Full          |     Dim    | FI, IM  |
| 0MOVE_TYPE_TEXT       | Movement Type - 0MOVE_TYPE_TEXT                             | Movement Type                                   | Full          |     Dim    | IM      |
| 0PLANT_ATTR           | Plant Master - 0PLANT_ATTR                                  | Plant Master                                    | Full          |     Dim    | IM      |
| 0PLANT_TEXT           | Plant Text - 0PLANT_TEXT                                    | Plant Text                                      | Full          |     Dim    | IM      |
| 0PROFIT_CTR_ATTR      | Profit Center Master - 0PROFIT_CTR_ATTR                     | Profit Center Master                            | Delta         |     Dim    | FI, IM  |
| 0PROFIT_CTR_TEXT      | Profit Center Text  -   0PROFIT_CTR_TEXT                    | Profit Center Text                              | Delta         |     Dim    | FI, IM  |
| 0RECIPCTRY_TEXT       | Customer Country - 0RECIPCTRY_TEXT                          | Customer Country                                | Full          |     Dim    | O2C     |
| 0SALES_OFF_TEXT       | Sales Office Text - 0SALES_OFF_TEXT                         | Sales Office Text                               | Full          |     Dim    | O2C     |
| 0SALESOFFICE_ORG_ATTR | Sales Office Organization Master - 0SALESOFFICE_ORG_ATTR    | Sales Office Organization Master                | Full          |     Dim    | O2C     |
| 0SALESORG_TEXT        | Sales Organization - 0SALESORG_TEXT                         | Sales Organization                              | Full          |     Dim    | O2C     |
| 0STOCKCAT_TEXT        | Stock Category - 0STOCKCAT_TEXT                             | Stock Category                                  | Full          |     Dim    | IM      |
| 0STOCKTYPE_TEXT       | Stock Category Text - 0STOCKTYPE_TEXT                       | Stock Category Text                             | Full          |     Dim    | IM      |
| 0STOR_LOC_TEXT        | Storage Location - 0STOR_LOC_TEXT                           | Storage Location                                | Full          |     Dim    | IM      |
| 0TRANSTYPE_ATTR       | Asset Transaction Type - 0TRANSTYPE_ATTR                    | Asset Transaction Type                          | Full          |     Dim    | FI      |
| 0TRANSTYPE_TEXT       | Asset Transaction Type Text - 0TRANSTYPE_TEXT               | Asset Transaction Type Text                     | Full          |     Dim    | FI      |
| 0VAL_CLASS_TEXT       | Valuation Class - 0VAL_CLASS_TEXT                           | Valuation Class                                 | Full          |     Dim    | IM      |
| 0VENDOR_ATTR          | Vendor Master - 0VENDOR_ATTR                                | Vendor Master                                   | Delta         |     Dim    | FI, IM  |
| 0VENDOR_TEXT          | Vendor Text - 0VENDOR_TEXT                                  | Vendor Text                                     | Delta         |     Dim    | FI, IM  |
| 1_CO_PA_DS2           | COPA Custom Extractor - 1_CO_PA_DS2                         | COPA Custom Extractor                           | Delta         |    Fact    | FI      |
| 2LIS_03_BF            | Goods Movements from Inventory Management - 2LIS_03_BF      | Goods Movements from Inventory Management       | Delta         |    Fact    | IM      |
| 2LIS_03_UM            | Inventory Revaluations - 2LIS_03_UM                         | Inventory Revaluations                          | Delta         |    Fact    | IM      |
| 2LIS_11_V_ITM         | Open Sales Order Lines - 2LIS_11_V_ITM                      | Open Sales Order Lines                          | Delta         |    Fact    | O2C     |
| 2LIS_11_V_SCL         | Allocation Scheduled Lines - 2LIS_11_V_SCL                  | Allocation Scheduled Lines                      | Delta         |    Fact    | O2C     |
| 2LIS_11_V_SSL         | Order Delivery Scheduled Lines - 2LIS_11_V_SSL              | Order Delivery Scheduled Lines                  | Delta         |    Fact    | O2C     |
| 2LIS_11_VAHDR         | Sales Document Header - 2LIS_11_VAHDR                       | Sales Document Header                           | Delta         |    Fact    | O2C     |
| 2LIS_11_VAITM         | Sales Document Line Items - 2LIS_11_VAITM                   | Sales Document Line Items                       | Delta         |    Fact    | O2C     |
| 2LIS_11_VAKON         | Sales Document Header Conditions - 2LIS_11_VAKON            | Sales Document Header Conditions                | Delta         |    Fact    | O2C     |
| 2LIS_11_VASCL         | Scheduled Line Items - 2LIS_11_VASCL                        | Scheduled Line Items                            | Delta         |    Fact    | O2C     |
| 2LIS_11_VASTH         | Sales Document Header Status - 2LIS_11_VASTH                | Sales Document Header Status                    | Delta         |    Fact    | O2C     |
| 2LIS_11_VASTI         | Sales Document Line Item Status - 2LIS_11_VASTI             | Sales Document Line Item Status                 | Delta         |    Fact    | O2C     |
| 2LIS_12_VCHDR         | Sales Delivery Header - 2LIS_12_VCHDR                       | Sales Delivery Header                           | Delta         |    Fact    | O2C     |
| 2LIS_12_VCITM         | Sales Delivery Line Items - 2LIS_12_VCITM                   | Sales Delivery Line Items                       | Delta         |    Fact    | O2C     |
| 2LIS_13_VDHDR         | Billing Document Header - 2LIS_13_VDHDR                     | Billing Document Header                         | Delta         |    Fact    | O2C     |
| 2LIS_13_VDITM         | Billing Document Line Items - 2LIS_13_VDITM                 | Billing Document Line Items                     | Delta         |    Fact    | O2C     |
| 2LIS_13_VDKON         | Billing Item Conditions - 2LIS_13_VDKON                     | Billing Item Conditions                         | Delta         |    Fact    | O2C     |
| ZSP_STOCK_IND         | Custom Stock Indicator - ZSP_STOCK_IND                      | Custom Stock Indicator                          | Full          |     Dim    | IM      |
| ZTCURR                | Custom Currency Extractor  - ZTCURR                         | Custom Currency Extractor                       | Full          |     Dim    | ALL     |
