# Lead-Quality-Analysis-for-Marketing-Campaigns

 This is a simplified subset of some data we have, one publisher (although multiple referring domains where traffic is sourced from) and one advertiser
This data shows what happened to about 3,000 leads that were sold to the advertiser; their ultimate disposition is in Column E. Every row is a "lead."
Our key questions are:
1. Are we seeing any lead quality trends over time (improving, declining)? Are they statistically
significant?
2. What can we learn about the drivers of "lead quality" from this dataset? What segments -
where the ad was shown, what kind of person filled out the ad, what kind of ad did they see -
have differing lead quality rates?
3. If the advertiser says they will increase our CPL by 20% (i.e., $30 to $33) if we increase our
lead quality by 20% (i.e., from 8.0% to 9.6%), do we see any opportunities to do that here? What kinds of things could we do?
Info you need to know
Column A: Lead created date
Column B: First name (you likely won't use this)
Column C: Email
Column D: VendorLeadID (you won't use this but its our unique key, good for counting in pivot tables) Column E: CallStatus. Every lead can only have one status. There are 4 groups of leads, though
1. Closed
2. leads that didn't close but the Advertiser would consider a sign of "good lead quality" - EP Sent,
Received, and Confirmed;
3. Leads the Advertiser would consider a sign of "bad lead quality" - unable to contact, invalid
profile and doesn't qualify; and
4. Unknown -- leads Advertiser considers a sign of neither bad nor good.
a. Closed - became a customer (this is the Advertisers' ultimate measure of success; they don't make money unless this happens -- the "best" quality lead by a longshot)
b. EP Sent - the first step in becoming a customer is to have an EP worksheet sent to you via email. If a person doesn't return their worksheet, they can stay in this status forever.
c. EP Received - the second step in becoming a customer is for the customer to have returned the worksheet
d. EP Confirmed - the third step is becoming a customer is for the Advertiser to confirm that all information in the worksheet is accurate and correc
e. Unable to Contact - this is a person who had a noncontactable phone number (fax line, disconnected line)
f. Contacted - Invalid Profile - Advertiser called the number and voice maail or person who answered was not the person from the lead info (phone number connected to Joe's Pizza shop, or person said "wrong number")

 g. Contacted - Doesn't Qualify - Advertiser called the number and talked to the right person, but they did not have enough debt to qualify for a program; or, they didn't have enough income to pay off their debts (perhaps unemployed right now
h. Unknown - all other states - talked to Advertiser but not interested after learning about the pros and cons of their program, person did not return voice mail, etc. Not a bad lead or a good lead
Column F: WidgetName. This is our internal name for the FormAd creative. Example: w-302252-DebtReduction1-1DC-yellowarrow-blue. 302252 means a 302x252 ad size. DebtReduction1 is a fieldset (set of questions asked -- in this case, they are all the same) - 1DC means all questions were on one form page; 2DC means they were on 2 different form pages; yellowarrow is a name for the design (see links below); and blue is color of background.
Note: 300250 and 302252 widgets are the same
Widget Name
Obviously one question would be whether WidgetName affects lead quality
Column G: PublisherZoneName. We actually have maybe 50 in our network, there are only 2 here. Refers to location on the page.
Column H: PublisherCampaignName. "DebtReductionInc Call Center" are leads created by people calling an 800# (and our call center staff entered the form information for the customer.) DebtReductionInc are leads that filled out the form online
Column I: AddressScore. We began receiving this information recently and don't have it for all dates. We checked the name and address against an offline database. 5 means the address matched the name perfectly; 4 and 3 are a close match; 2 or 1 means the address didn't match the name.
Column J: PhoneScore. We began receiving this information recently and don't have it for all dates. We checked the name and address against an offline database. 5 means the address matched the name perfectly; 4 and 3 are a close match; 2 or 1 means the address didn't match the name.
Column K: AdvertiserCampaignName. creditsolutions-branded-shortform indicates consumers saw the Advertisers logo on the ad; Debt Settlement1 Master means it was a generic form (did not mention advertiser's name)
Column L: State that the Consumer lives in
Column M: Debt level. Amount of debt the consumer has
Column N: IP Address (I deleted them, there are things we can do resolving these to home/work but you can ignore for these purposes)

 Column O: Partner -- this dataset is internal advertising we're doing on google, yahoo, adknowledge, etc. This is the company who ran ads driving to the site (DebtReductionInc.com) where our test ads ran
Column P: Referral domain - URL of domain that drove the traffic to the website where our test ads ran
Column Q: Campaign -- Google AdWords or Yahoo Search Marketing campaign name. If it says "content" it isn't search traffic but AdSense traffic from Google's content network
Column R: AdGroup - Google AdWords or Yahoo Search Marketing AdGroup.
Column S: Keyword - Google AdWords or Yahoo Search Marketing Keyword
Column T: Referring Keyword String - actual keyword string typed in by the user (if applicable) Column U: Referral URL
Column V: Referral URL parameters - other strings after the referral url
Column W: LandingPage URL (what page the ad was shown on)
Column X: LandingPageURL parameters - other strings after the landing page url, mostly already parsed into Columns P-T
