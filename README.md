DCHBX Health Exchange Plans
===========================

Parses plan info from the DC health exchange, as gotten from
a Freedom of Information Act request.


### Example Plan

Here's what the data for a plan looks like (with a lot of `coverage` choices and `rate` details cut out):

```json
{
  "77422DC0060001": {
    "coverage": {
      "Abortion for Which Public Funding is Prohibited": {
        "is_covered": "Not Covered"
      },
      "Accidental Dental": {
        "ehb_variance_reason": "Additional EHB Benefit",
        "excluded_from_in_network_moop": "No",
        "excluded_from_out_of_network_moop": "No",
        "exclusions": "Member cost share based on place and type of service.",
        "is_covered": "Covered",
        "quantitative_limit": "No",
        "subject_to_deductible_t1": "Yes",
        "subject_to_deductible_t2": "No"
      },
      "Acupuncture": {
        "is_covered": "Not Covered"
      },
      "Allergy Testing": {
        "ehb": "Yes",
        "excluded_from_in_network_moop": "No",
        "excluded_from_out_of_network_moop": "No",
        "exclusions": "Member cost share based on place and type of service.",
        "is_covered": "Covered",
        "quantitative_limit": "No",
        "subject_to_deductible_t1": "Yes",
        "subject_to_deductible_t2": "No"
      },
      "Bariatric Surgery": {
        "is_covered": "Not Covered"
      },
      "Basic Dental Care \u2013 Adult": {
        "is_covered": "Not Covered"
      },
      "Basic Dental Care \u2013 Child": {
        "ehb_variance_reason": "Other Law/Regulation",
        "exclusions": "Minor restorative services include amalgam fillings on posterior teeth and resin composite filling on anterior teeth.  Periodontal root Planning and scaling are limited to 4 separate quadrants every two (2) rolling years.  A number of Basic services listed in this Plan are subject to a dental review or an alternate benefit may be paid.  General anesthesia and intravenous sedation, when specifically covered, and only when done in connection with another medically necessary covered service or supply is eligible.\n",
        "is_covered": "Not Covered"
      },
      "Chemotherapy": {
        "ehb": "Yes",
        "excluded_from_in_network_moop": "No",
        "excluded_from_out_of_network_moop": "No",
        "exclusions": "Member cost share based on place and type of service.",
        "is_covered": "Covered",
        "quantitative_limit": "No",
        "subject_to_deductible_t1": "Yes",
        "subject_to_deductible_t2": "No"
      }
    },
    "id": "77422DC0060001",
    "issuer": {
      "id": 77422,
      "is_dental_only": false,
      "issuer_state": "DC",
      "market": "Individual",
      "tin": "06-6033492"
    },
    "metadata": {
      "brochure_url": "http://www.aetna.com/individuals-families-health-insurance/buy-insurance/exchange/dc.html",
      "child_only_offering": "Allows Adult and Child-Only",
      "disease_management_program_offered": "Heart Disease, Diabetes",
      "formulary_id": "DCF001",
      "hios_product_id": "77422DC006",
      "hsa_elligible": "No",
      "limited_cost_sharing_plan_variation_est_adv_payment": 0,
      "metalic_level": "Bronze",
      "national_network": "No",
      "network_id": "DCN001",
      "new_or_existing_plan": "New",
      "notice_required_for_pregnancy": "No",
      "out_of_country_coverage": "No",
      "out_of_service_area_coverage": "Yes",
      "out_of_service_area_coverage_description": "Covered With Limitations.",
      "plan_effective_date": "2014-01-01T00:00:00",
      "plan_name": "Aetna Advantage 5750",
      "plan_type": "PPO",
      "qhp": "On the Exchange",
      "referral_required_for_specialist": "No",
      "sbc_url": "http://www.aetna.com/individuals-families-health-insurance/buy-insurance/exchange/dc.html",
      "service_area_id": "DCS001",
      "unique_plan_design": "Yes",
      "wellness_program_offered": "Yes"
    },
    "rates": [
      {
        "age": "0-20",
        "effective": "2014-01-01T00:00:00",
        "expires": "2014-12-31T00:00:00",
        "rate": 181.27,
        "rating_area": "Rating Area 1",
        "tobacco_use": "No Preference"
      },
      {
        "age": 21.0,
        "effective": "2014-01-01T00:00:00",
        "expires": "2014-12-31T00:00:00",
        "rate": 201.5,
        "rating_area": "Rating Area 1",
        "tobacco_use": "No Preference"
      },
      {
        "age": 22.0,
        "effective": "2014-01-01T00:00:00",
        "expires": "2014-12-31T00:00:00",
        "rate": 201.5,
        "rating_area": "Rating Area 1",
        "tobacco_use": "No Preference"
      },
      {
        "age": 23.0,
        "effective": "2014-01-01T00:00:00",
        "expires": "2014-12-31T00:00:00",
        "rate": 201.5,
        "rating_area": "Rating Area 1",
        "tobacco_use": "No Preference"
      }
    ]
  }
}
```