# A-B-Test

# Eniac Conversion Optimization Project

Welcome to the Eniac Conversion Optimization Project! This project focuses on evaluating and enhancing the user experience on Eniac’s website to increase conversions, specifically aiming to boost iPhone 13 sales.

## Project Overview

The Data team at Eniac is tasked with analyzing which version of a website feature converts more visits to sales. The primary objective is to improve the conversion rate for the iPhone 13 by testing different design elements and user interactions on the website.

## Customer Journey

The steps needed for a user to purchase the iPhone 13 are as follows:

1. Visit Eniac’s site.
2. Click on the “SHOP NOW” button in the iPhone banner.
3. Click on the model to purchase (13, 13 Pro, 13 Pro Max…).
4. Add the product to the shopping basket.
5. Go to the “Check-out” page.
6. Add the delivery details.
7. Add the payment details.
8. Confirm the purchase.

## Conversion Funnel

From Eniac's web traffic (50,000 visits in one week), only a small portion of visitors convert into buyers, resulting in 30 iPhone sales. The funnel stages and their conversion rates are critical to understand where potential buyers drop off:

- Visits to Site
- Clicks on “SHOP NOW” Button
- Model Selection
- Add to Basket
- Check-out
- Delivery Details
- Payment Details
- Purchase Confirmation

## Key Metrics

### Conversion Rates

Conversion rates help determine the efficiency of each funnel step:

- Top of the Funnel: The “SHOP NOW” button has a 2% conversion rate.
- Middle and Bottom of the Funnel: Subsequent steps have conversion rates of more than 30%.

![image](https://github.com/NuriaAmezaga/A-B-Test/assets/168557674/63b276cb-b4ef-432c-815a-7c121dca76b7)

### Click-Through Rate (CTR)

With the goal of increasing the conversion rate of the “SHOP NOW” button, marketing has asked the Design team for a redesign of the button, resulting in the following versions:

- **Version A**: The original site.
- **Version B**: The “SHOP NOW” button is now red.
- **Version C**: The “SHOP NOW” button has a new text, “SEE DEALS”.
- **Version D**: Both the changes from Version B and Version C have been applied.

  ![image](https://github.com/NuriaAmezaga/A-B-Test/assets/168557674/36705182-7a82-49b7-9a61-5bbcbe7f0fe5)


### Experimentation and Analysis

While exploring the data from the different versions of the website, that they had strong differences in click-through rates. Those rates can be calculated by simply dividing the clicks that each element of interest got (the elements “SHOP NOW” and “SEE DEALS”) by the overall number of visits on each page.

It seems like the red variations are the worst performers, while the white buttons perform much better. But, are those differences due to chance? 

- **Null Hypothesis**: The 4 versions of the button are equally likely to receive clicks, and the observed differences are due to chance.
- **Alternative Hypothesis**: The observed differences are not due to chance: there is at least one version that got so many more/much fewer clicks than the others that this can hardly be explained just by chance.

We perform a chi-square test using the `chi2_contingency` function from `scipy`, and finally see whether the results are significant. 

## Results

The version with the highest click-through rate, Version C, exhibits a statistically significant difference when compared to Versions B and D, but not to Version A, which possesses the second-highest click-through rate. As a result, declaring a clear winner based on post hoc tests becomes challenging. Therefore, we can only say that both Version C and Version A are the winners.

However, if a definitive winner is required, additional steps need to be implemented. This is where we transition from the realm of statistics to the business world. The following actions can help in determining the version to be featured on the website in the future:

- Consider other metrics alongside the click-through rate.
- Incorporate qualitative research findings.
- Seek input from subject-matter experts.
- Redesign the experiment and conduct it once more.

## Conclusion

Through this project, I have learned about the possible statistical performances and how to interpret the results effectively. Even when the significant statistics are not clear, taking into account other metrics implicated in the business world is very useful. These additional insights can provide a more comprehensive understanding of user behavior and guide better decision-making for future optimizations.

