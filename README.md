# Senior Customer Support Engineering Take Home Assessment

## Getting Started

- \[x] Before you start, you'll need a GitHub, GitLab or Bitbucket account.
  - https://github.com/rishi-raj-jain
- \[x] If you haven't already, create a free Hobby account on Vercel. You can sign up to Vercel by using your GitHub, GitLab, or BitBucket account.
  - https://vercel.com/rishi-raj-jain
- \[x] Then, create a Next.js project on Vercel. You can use our get started guide,
documentation and templates for help and inspiration.
  - https://vercel.com/rishi-raj-jain/my-nextjs-project

## The Exercise

#### 1. From [this list](https://gist.github.com/Pieparker/b04a4e9ff82ba949e5db9d5b0e9d89e8), rank your 5 most favourite and 5 least favourite support tasks. Provide a brief explanation for each.

Even though I accept the work as is (regardless of the task category) and discuss the priorities with my manager, here are my top 5 **most favourite** tasks from the given list:

- Write and maintain support articles and docs pages: I have written over [50 technical articles](https://rishi.app/blogs/#:~:text=READ%20MORE%20%E2%86%92-,Media%20Posts,-Using%20Astro%20and) that have been published by Xata, Upstash, Storyblok, HarperDB, Koyeb, etc. I enjoy technical writing because it educates, allows the readers to save time and learn from the existing set of approaches. With support articles and docs pages, the ideal/expected use of the technology in a given use case is communicated clearly. In addition, edge cases are specifically highlighted to inform the users of the features/tradeoffs.
- Create video tutorials to help teach users a specific feature or use case: I truly believe in documenting solutions, videos being one of the mediums. The process of learning/implementing a use case by a customer/enthusiast becomes easier as they're being visually guided by the video tutorials throughout. Here are the [videos](https://rishi.app/videos/) that I have created in the past revolving around web developement.
- Identify, file (and, where possible, resolve) bugs in private and public Vercel/Next.js repos on GitHub: The best way to learn is by doing. I have (in my earlier roles) dug into unknown big projects and identified the gaps where the customer/enthusiast can improve in their production ready code/POCs to make the best use of the technology. This allows to identify if any gaps in the documentation that needs to be covered, and improves my technical knowledge/expertise in doing so.
- Work with the product team to develop a new feature based on feedback from customers: Customer are the core of business. Being at front of the line, it'd help me gather feedback from the customers and propose a new feature/idea/project to address the commonly raised issues/requests. Further, using the feedback loop, the team can re-iterate to address the needs of the customer better, and have a better chance of converting the enthusiasts to customers.
- Respond to queries on Twitter, Reddit, Hacker News and other 3rd party sites: While emails are great, people often take to social media (including myself in the past) to raise technical issues, say out of frusturation. In addition to that, the social media presence of `rauchg` is a demonstration of how even CEOs are fielding customer/enthusiast's questions during weekends and ONLY sticking to the subject of matter. This creates a positive effect for the observers and resolves the issue(s).

Alright, let's get to the 4 **least favourite** tasks (though I'd like to highlight that work is work and there are no two ways about it):

- Help resolve billing issues for customers: I've been a Support Engineer at Lemon Squeezy, and there were huge inbound of payment related tickets and I am aware that billing is the most concerned parts for any customer.  I'm more than happy to run the playbooks and/or escalate the issue via process to the Billing team so that the team can focus on their areas of expertise.
- Manage a support team: I'd like to gain more experience in handling customer issues first.
- Find and recruit teammates for the support team: Even though I'm more than happy to do interviews for teammates, this is something that I'd address this after the customer's needs.
- Analyze hundreds of support tickets to spot trends the product team can use: While this is something that can be done in parallel to addressing the support tickets, by let's say using categories to mark a support ticket and reference them later, I'd address this after the customer's needs.
- I couldn't find the 5th as all other choices seemed of my immediate interests and definitely NOT fall in least favourite zone.

#### 2. What do you want to learn or do more of at work?

I am a fan of Vercel since I attended the first Zeit Hackathon. At Vercel, I aim to learn and do more of the following:

- Be at the front of the line to respond **quickly** to customer/ethusiast issue(s).
- Be **highly** involved in addressing technical difficulties faced with the platform.
- **Bridge** the gap between developer and Vercel by contributing to SDKs and Docs/Videos.
- Learn about and improve the knowledge of **numerous** production-ready architecture possible with Vercel.

#### 3. Describe how you solved a challenge or technical issue that you faced in a previous role (preferably in a previous support role). How did you determine that your solution was successful?

TODO

#### 4. When would you choose to use Edge Functions, Serverless Functions, or Edge Middleware with Vercel?

TODO

#### 5. Imagine a customer writes in requesting help with a build issue on a framework or technology that you've not seen before. How would you begin troubleshooting this and what questions would you ask the customer to understand the situation better?

TODO

#### 6. Please write a follow-up reply to the customer.

TODO

#### 7. A customer writes in to the Helpdesk asking "How do I do a redirect from the /blog path to https://example.com?" Please write a reply to the customer. Feel free to add any information about your decision making process after the reply.

<hr />

Hey there,

Using [Redirects](https://vercel.com/docs/edge-network/redirects) you can redirect an incoming request to a given URL. The redirects are populated to every deployment region's edge network.

- If you're using Next.js for your project, make the following additions in next.config.(mjs|ts|js) file of your project:

```diff
// ...

module.exports = {
  // ...,
+  async redirects() {
+     return [
+       {
+         source: '/blog',
+         destination: 'https://example.com',
+         permanent: true,
+       },
+     ];
+   },
}
```

- If you're not using Next.js, create (or update) a `vercel.json` at the root directory of your project with the following code:

```json
{
  "redirects": [
    {
      "source": "/blog",
      "destination": "https://example.com",
      "permanent": true
    }
  ]
}
```

and deploy the changes to Vercel to see the redirection in effect.

Hope this helps. Do let us know if anything.

<hr />

Thought process: Each customer wants to use a service to focus on their business logic. If a customer faces an issue, even though it's tempting to educate them in detail about the platform and it's benefits, the immediate response the support engineer can get out to them is the solution that they need. This addresses the pain point of the user, and then one can proceed to educate and showcase the benefits in further communication. In this case, the customer needed to learn how to redirect, I could have asked them about their stack and wait for some hours before they respond. But the likelihood of it being not addressed by the response I sent above is not worth hours of wait, so I responded to them with an answer that is most likely to address the concern.

#### 8. A customer is creating a site and would like their project not to be indexed by search engines. Please write a reply to the customer. Feel free to add any information about your decision making process after the reply.

TODO

#### 9. What do you think is one of the most common problems which customers ask Vercel for help with? How would you help customers to overcome common problems, short-term and long-term?

TODO

#### 10. How could we improve or alter this familiarisation exercise?

I think the use of Next.js is confusing for this exercise. I am more than happy to spin up a Next.js project, but unless I am developing an application using it, I do not see the immediate use of it in this exercise.
