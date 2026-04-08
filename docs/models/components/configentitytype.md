# ConfigEntityType

Entity types for the API configuration.

This enum contains all valid entity type configurations that users can specify:
- Parent types (e.g., "name", "financial_id") that expand to all subtypes
- Specific subtypes using dot notation (e.g., "name.full_name")
- Standalone terminal types (e.g., "email_address")

When converted for service use, parent types expand to all their terminal subtypes.

## Example Usage

```go
import (
	"github.com/bdlilley/elevenlabs-go/models/components"
)

value := components.ConfigEntityTypeName

// Open enum: custom values can be created with a direct type cast
custom := components.ConfigEntityType("custom_value")
```


## Values

| Name                                                                  | Value                                                                 |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `ConfigEntityTypeName`                                                | name                                                                  |
| `ConfigEntityTypeNameNameGiven`                                       | name.name_given                                                       |
| `ConfigEntityTypeNameNameFamily`                                      | name.name_family                                                      |
| `ConfigEntityTypeNameNameOther`                                       | name.name_other                                                       |
| `ConfigEntityTypeEmailAddress`                                        | email_address                                                         |
| `ConfigEntityTypeContactNumber`                                       | contact_number                                                        |
| `ConfigEntityTypeDob`                                                 | dob                                                                   |
| `ConfigEntityTypeAge`                                                 | age                                                                   |
| `ConfigEntityTypeReligiousBelief`                                     | religious_belief                                                      |
| `ConfigEntityTypePoliticalOpinion`                                    | political_opinion                                                     |
| `ConfigEntityTypeSexualOrientation`                                   | sexual_orientation                                                    |
| `ConfigEntityTypeEthnicityRace`                                       | ethnicity_race                                                        |
| `ConfigEntityTypeMaritalStatus`                                       | marital_status                                                        |
| `ConfigEntityTypeOccupation`                                          | occupation                                                            |
| `ConfigEntityTypePhysicalAttribute`                                   | physical_attribute                                                    |
| `ConfigEntityTypeLanguage`                                            | language                                                              |
| `ConfigEntityTypeUsername`                                            | username                                                              |
| `ConfigEntityTypePassword`                                            | password                                                              |
| `ConfigEntityTypeURL`                                                 | url                                                                   |
| `ConfigEntityTypeOrganization`                                        | organization                                                          |
| `ConfigEntityTypeFinancialID`                                         | financial_id                                                          |
| `ConfigEntityTypeFinancialIDPaymentCard`                              | financial_id.payment_card                                             |
| `ConfigEntityTypeFinancialIDPaymentCardPaymentCardNumber`             | financial_id.payment_card.payment_card_number                         |
| `ConfigEntityTypeFinancialIDPaymentCardPaymentCardExpirationDate`     | financial_id.payment_card.payment_card_expiration_date                |
| `ConfigEntityTypeFinancialIDPaymentCardPaymentCardCvv`                | financial_id.payment_card.payment_card_cvv                            |
| `ConfigEntityTypeFinancialIDBankAccount`                              | financial_id.bank_account                                             |
| `ConfigEntityTypeFinancialIDBankAccountBankAccountNumber`             | financial_id.bank_account.bank_account_number                         |
| `ConfigEntityTypeFinancialIDBankAccountBankRoutingNumber`             | financial_id.bank_account.bank_routing_number                         |
| `ConfigEntityTypeFinancialIDBankAccountSwiftBicCode`                  | financial_id.bank_account.swift_bic_code                              |
| `ConfigEntityTypeFinancialIDFinancialIDOther`                         | financial_id.financial_id_other                                       |
| `ConfigEntityTypeLocation`                                            | location                                                              |
| `ConfigEntityTypeLocationLocationAddress`                             | location.location_address                                             |
| `ConfigEntityTypeLocationLocationCity`                                | location.location_city                                                |
| `ConfigEntityTypeLocationLocationPostalCode`                          | location.location_postal_code                                         |
| `ConfigEntityTypeLocationLocationCoordinate`                          | location.location_coordinate                                          |
| `ConfigEntityTypeLocationLocationState`                               | location.location_state                                               |
| `ConfigEntityTypeLocationLocationCountry`                             | location.location_country                                             |
| `ConfigEntityTypeLocationLocationOther`                               | location.location_other                                               |
| `ConfigEntityTypeDate`                                                | date                                                                  |
| `ConfigEntityTypeDateInterval`                                        | date_interval                                                         |
| `ConfigEntityTypeUniqueID`                                            | unique_id                                                             |
| `ConfigEntityTypeUniqueIDGovernmentIssuedID`                          | unique_id.government_issued_id                                        |
| `ConfigEntityTypeUniqueIDAccountNumber`                               | unique_id.account_number                                              |
| `ConfigEntityTypeUniqueIDVehicleID`                                   | unique_id.vehicle_id                                                  |
| `ConfigEntityTypeUniqueIDHealthcareNumber`                            | unique_id.healthcare_number                                           |
| `ConfigEntityTypeUniqueIDHealthcareNumberMedicalRecordNumber`         | unique_id.healthcare_number.medical_record_number                     |
| `ConfigEntityTypeUniqueIDHealthcareNumberHealthPlanBeneficiaryNumber` | unique_id.healthcare_number.health_plan_beneficiary_number            |
| `ConfigEntityTypeUniqueIDDeviceID`                                    | unique_id.device_id                                                   |
| `ConfigEntityTypeUniqueIDUniqueIDOther`                               | unique_id.unique_id_other                                             |
| `ConfigEntityTypeMedical`                                             | medical                                                               |
| `ConfigEntityTypeMedicalMedicalCondition`                             | medical.medical_condition                                             |
| `ConfigEntityTypeMedicalMedication`                                   | medical.medication                                                    |
| `ConfigEntityTypeMedicalMedicalProcedure`                             | medical.medical_procedure                                             |
| `ConfigEntityTypeMedicalMedicalMeasurement`                           | medical.medical_measurement                                           |
| `ConfigEntityTypeMedicalMedicalOther`                                 | medical.medical_other                                                 |