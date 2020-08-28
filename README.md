# Discussion 28.08.20

## Initial assumptions:

* we took a look on https://github.com/Archi-Lab/fae-team-4/wiki/Christian-Fr%C3%B6hlingsdorf-Challenges-in-the-Field-of-Dynamic-UI-Composition-for-Microservices
* no context was provided, so we brainstormed rather than audited
* we found your implementation of similar architecture https://github.com/rewe-digital-incubator/composer
* we assume your use-case are more like "e-commerce web page" than "enterprise SPA application" to deliver best time-to-first-byte and foster SEO

## What we liked:

* server-side composition is better than client-side (for your use-cases)
* we also prefer run-time integration over build-time integration to avoid lockstep release process
* having your own library/framework is better than using other vendor library/framework (in order not to introduce unnecessary complexity)
* we liked the DDD structure of your wiki 
* micro frontend libraries/frameworks/best practices are still terra incognita in 2020, so this is an amazing moment to build something popular and helpful

## What probably might be improved:

* original Field-of-Dynamic-UI-Composition-for-Microservices document says nothing about not having a single point of failure, this is probably taken-care of using regular means for stateless web services, and it should be
* rewe-digital/composer has a very initial version of template validation
* both solutions have a quite trivial way to handle CSS separation via prefixes
* it might be worthwhile to consider modular/plugin architecture for library
* MFs communication is vaguely described
* there is nothing about feature flags, maybe this is outside of the scope; however, FF mixes well with micro frontends based on our experience

## Our ideas what we can accomplish together

* port current digital-incubator/composer or another library to .NET Core to provide better adaptability
* use Contract Tests for MFs to provide better robustness the same way as contract tests help with backend microservices
* implement modular/plugin architecture
* use Dhall language to have DUC configuration/templating less error-prone
* benchmark your solution against https://www.mosaic9.org/ and provide lessons learned document

## Our experience

* https://www.insightguides.com/ -> not really MF, but quite interesting learning lesson how to mix SSR and SPA building e-commerce site using meteor (project started in 2015 and predates angular/react/vue)
* https://www.rydoo.com/ -> tribes builds MF as few web applications (routing via app1.domain app2.domain), common style guide and common session to provide team scalability



