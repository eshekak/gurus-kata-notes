# Martin Fowler's Blog
> https://martinfowler.com

1. [APIs should not be copyrightable](https://martinfowler.com/articles/copyright-api.html)
> **APIs should not be copyrightable.** You should be able to copyright a software component, but not its interface.
> So that programmers can reimplement its interface with another implementation to support: interoperability, 
> testing and competition.

2. [AccessModifier](https://martinfowler.com/bliki/AccessModifier.html)
> **Access control does not control access** If you have a field that's private it means no other class can get at it.
> Wrong! If you really want to you can subvert the access control mechanisms in almost any language. Usually the way 
> through is via reflection. The rationale is that debuggers and other system tools often need to see private data, 
> so usually the reflection interfaces allow you to do this.

3. [DDD_Aggregate](https://martinfowler.com/bliki/DDD_Aggregate.html)
> **A DDD aggregate is a cluster of domain objects that can be treated as a single unit.** An example may be an order and 
> its line-items, these will be separate objects, but it's useful to treat the order (together with its line items) as 
> a single aggregate.

> An aggregate will have one of its component objects be the aggregate root. Any references from outside the aggregate 
> should only go to the aggregate root. The root can thus ensure the integrity of the aggregate as a whole.
  
> Aggregates are the basic element of transfer of data storage - you request to load or save whole aggregates. 
> Transactions should not cross aggregate boundaries.

4. [Agile Brazil Interview](https://www.infoq.com/interviews/fowler-caroli-continuous-deployment/)
> **What to do when acceptance tests take a lot of time?** We have two layers of test. First layer is a fast moving set 
> of unit tests that gives you a quick feedback. Then, you have the acceptance tests that do run through the browser 
> that do have things like databases connected, running on a separate stage of the pipeline. Also you can run your 
> acceptance tests in parallel. Of course, their correct execution depends on the power of machines and there is no 
> dependency of one test on the other.

> **What would be a short time for build to have the feedback?** For the commit stage, you want 10 minutes or less.

> **Polyglot programming. What do you think about it?** The idea of using different languages for different strengths,
> that’s what polyglot programming is about. There is a separate point. I think the pragmatic programmers advice try 
> to learn a new different language (if you already know Java, learning C# doesn’t count) every year and not necessarily
> a language that you expect to use day-to-day in your production programming work, but one that will stretch your mind 
> in a different direction, open new possibilities.

> **How early and how continuously should we deliver?** As early as possible, but always the top quality. You want to go into 
> production, as rapidly as you possibly can and then you want to be cycling updates as quickly as you can, as well. 
> There is still attenuation here from how rapidly the customer wants to get something, wants the minimal thing that
> they can go with first.

5. [AgileImposition](https://martinfowler.com/bliki/AgileImposition.html)
> **As a methodology or design approach becomes fashionable, then we see a lot of people using it, or teaching it, who are 
> focusing on the fashion rather than the real details.** This can lead to reports of things done in agile's name which
> are a polar opposite to the principles of movement's founders. For example, imposing a process on a team is completely
> opposed to the principles of agile software, and has been since its inception.

6. [An Appropriate Use of Metrics](https://martinfowler.com/articles/useOfMetrics.html)
> **Metrics cannot be used as a substitute for thinking. So organizations must be vigilant against the undesirable 
> behaviors that emerge due to the inappropriate use of metrics.**

> **Guidelines for a more appropriate use of metrics:**
* **Explicitly link metrics to goals.** Management is responsible for ensuring the end goal is always kept in sight, working with the people with the most knowledge of the system to come up with measures that make the most sense to monitor for progress.
* **Favor tracking trends over absolute numbers.** Focusing on trends is important because it provides feedback based on real data on any change implemented and creates more options for organizations to react.
* **Use shorter tracking periods.** Organizations benefit from using shorter tracking periods as it creates more opportunities for re-planning that allows maximum value.
* **Change metrics when they stop driving change.** Organizations need to drop metrics that are no longer relevant.

7. [AbundantMutation](https://martinfowler.com/bliki/AbundantMutation.html)
> **Evolutionary Design expects the team to modify the design as the project proceeds; both to cope with requirements 
> changes and to take advantage of learning.** But evolutionary design requires attention, skill, and leadership. It's just 
> a different sort of leadership than many commonly think.


8. [ActivityOriented](https://martinfowler.com/bliki/ActivityOriented.html) and [OutcomeOriented](https://martinfowler.com/bliki/OutcomeOriented.html)
> **A mandate to deliver a business outcome is very different from a mandate to deliver a certain amount of scope. Scope delivery is easy, relatively speaking.** Outcome realization requires real collaboration between those who understand the problem and those who can fashion various levels of solution for it. Initial attempts at solution lead to a better understanding of the problem which leads to further attempts at better solutions. This doesn’t work where the product management organization is separate from the development (scope-delivery) organization.

> Outcome-oriented teams are necessarily cross-functional (multidisciplinary) whereas ActivityOriented teams are typically mono-functional (single specialty). In the most traditional scenario, an outcome might simply be defined in terms of a project. The project is funded on the basis of a business case and therefore the desired outcome is to realize what is promised in the business case. However, depending on the size of the project it may be organized as one or more teams. When these teams are set up along activity boundaries it becomes an activity-oriented project (or program) organization. On the other hand, we achieve an outcome-oriented organization by dividing the overall outcome into sub-outcomes and assigning sub-outcomes to cross-functional teams that are self-sufficient in terms of people required to deliver the sub-outcome.