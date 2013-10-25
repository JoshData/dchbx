DCHBX Health Exchange Plans
===========================

The District of Columbia elected to create its own health insurance marketplace, which is DCHealthLink.com. I FOIA'd the DC Health Benefit Exchange Authority (DCHBX), the agency in charge of the marketplace, for a list of all of the plans offered on the exchange. (See my [FOIA request](https://github.com/JoshData/dchbx/blob/master/foia_log.html).)

It's all Excel spreadsheets, and kind of a mess, but it's fascinating. It has:

* Plan names for plans available on DCHealthLink (individual and Small Business Health Options Program (SHOP) plans)
* Price by age of applcant.
* Tables of benefits of covered services.
* Tables of copay rates, deductibles, and so on.
* Lots of other things I don't understand.

Here are the files as I received them:

http://razor.occams.info/files/dchbx_plans_20131024.zip

I've written a scraper to convert some of this information to JSON. An example from plans.json is below.

### Example Plan

Here's what the data for a plan looks like (with a lot of `coverage` choices, `rate` details, and various other fields cut out):

```json
{
  "77422DC0060001": {
    "coverage": {
      "Acupuncture": {
        "is_covered": "Not Covered"
      }, 
      "Allergy Testing": {
        "costs": {
          "Coinsurance": {
            "In Network (Tier 1)": "No Charge", 
            "Out of Network": "50% Coinsurance after deductible"
          }, 
          "Copay": {
            "In Network (Tier 1)": "$40 Copay after deductible", 
            "Out of Network": "No Charge"
          }
        }, 
        "exclusions": "Member cost share based on place and type of service.", 
        "is_covered": "Covered", 
        "quantitative_limit": "No", 
        "subject_to_deductible_t1": "Yes", 
        "subject_to_deductible_t2": "No"
      }, 
      "Basic Dental Care \u2013 Adult": {
        "is_covered": "Not Covered"
      },
    },
    "deductibles": {
      "Combined Medical and Drug EHB Deductible": {
        "Combined In/Out Network": {
          "Family": "Not Applicable", 
          "Individual": "Not Applicable"
        }, 
        "In Network": {
          "Default Coinsurance": 0, 
          "Family": 11500, 
          "Individual": 5750
        }, 
        "In Network (Tier 2)": {}, 
        "Out of Network": {
          "Family": 23000, 
          "Individual": 11500
        }
      }, 
    },
    "id": "77422DC0060001",
    "issuer": {
      "id": 77422,
      "is_dental_only": false,
      "issuer_state": "DC",
      "market": "Individual",
      "tin": "06-6033492"
    },
    "maximums": {
      "Maximum Out of Pocket for Medical and Drug EHB Benefits (Total)": {
        "Combined In/Out Network": {
          "Family": "Not Applicable", 
          "Individual": "Not Applicable"
        }, 
        "In Network": {
          "Family": 12700, 
          "Individual": 6350
        }, 
        "In Network (Tier 2)": {}, 
        "Out of Network": {
          "Family": 25400, 
          "Individual": 12700
        }
      }, 
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