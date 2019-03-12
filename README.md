# C4-PlantumlSkin
Some skinning to create C4 diagrams

## Prerequisites
---

Before you start, you need to be familiar at minimum with:

- [PlantUml](http://plantuml.com/index)
- [C4 model](https://c4model.com/)

First of all you need to have plantuml up and running. For this you have multiple options (all of which will work with this):

1. [Local installation](http://plantuml.com/starting)
1. [Free online editor](http://www.plantuml.com/plantuml/uml/5Oqn3W8X44LxJw47a6csijh42vXu0XOcGdOO2FCdNb-iNbxptcw84zxaSgkQn3Fxb6i1XZs8Plo6JqNnmurdwWfMXDGRsIaS5QMxqNExlsJ9ghpFgjIYWISTNYLJTmm7fIsC_sLdpOi_) <-- This is ready for you to start creating C4 models!!
1. [Another free online editor](https://www.planttext.com/)
1. [VisualStudio Code Plugin](https://github.com/qjebbs/vscode-plantuml): This plugin allows you to "embed" diagrams in your markdown files, which is the best of all worlds in my opinion, and is hence really recommended.

Once you have something running (or just went to planttext online editor), you can start using plantuml to create text-driven models and diagrams.

## Quickstart
---

Assuming that you have an environment that you can use PlantUml, add the following line:
```plantumlcode
!includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml
```
Just below `@startuml`, and then use the following components with the specified stereotype:

| C4 artifact | PlantUml | Stereotype for internal | Stereotype for external |
|---|---|---|---|
| Person | `actor` | `<<Internal>>` | `<<External>>` |
| System | `frame` | `<<Internal System>>`, <br> `<<Internal>>`, <br> or `<<System>>` | `<<External System>>` <br> or `<<External>>` |
| System | `rectangle` | `<<Internal System>>` <br> or `<<System>>` | `<<External System>>` |
| Containers | `component` | `<<Internal Container>>`, <br> `<<Internal>>`, <br> or `<<Container>>` | `<<External Container>>` <br> or `<<External>>` |
| Containers | `rectangle` | `<<Internal Container>>` <br>or `<<Container>>` | `<<External Container>>` |
| Component | `rectangle` | `<<Internal Component>>` <br> or `<<Component>>` | `<<External Component>>` |
| Database | `database` | `<<Internal Database>>` <br> or `<<Internal>>` |  `<<External Database>>` <br> or `<<External>>` |
| Queue | `queue` | `<<Internal Queue>>` <br> or `<<Internal>>` |  `<<External Queue>>` <br> or `<<External>>` |
| Expanded systems, <br> containers and components | `frame`, <br> `component`, <br> or `rectangle` <br> according to your need | `<Expanded>` | `<Expanded>` |

## Examples
---

Reproduced (as closely as possible from diagrams from [the official C4 model website](https://c4model.com/))

1. System Context diagram

    [PlantUml file for diagram below](./sample/c4-banking-system.puml)

    [Edit this diagram online!](http://www.plantuml.com/plantuml/uml/jP8_Rzim4CLtVefhHgEH5az1OAGDF6G8423PcY0uKsUBCFy8l6FjeEXtxrcIvTG1sYuLj8ZwlSVtUBnXmImbUFF9HUjBGoLxQ4KwlghhZBjguwGjgyAKROf2KIgRGirRJnYbJONhs_dbWyTuS7dSkbW7PA5ShuhpJPsAT4LgEw-wmov6d7Y2hnYLt02_AHgCnKvSYl3KEWPzfJqXZpq2jCVGgL9mIn7MEOKffPs7r93lSvbCLZ1kbAI0ph_o8B--NkurL4G_6YuMyCs0FhFPyl90ZbbcCzClFsa45mV5lRCvSLeBBFUsLNVg4NglCo_QBMr8esVuqVz7Aod3nGDbJcepDNgEjuKb1SeNckikZha6JdCXWns18Skfa-jXajVLu3NfF_OQkjsDWhFZr9OJzCNxj3jjoI09lZlQJO2BwvG3zXF2LIe2Mj9bE6JuF55eRIfH630s47HAqE5R85tfaPVpAW7LDsEWKnUTqP-wt1yL_wlCltVvQSnn2wYQj8lLukDihg0miJbVdmJJ2VnTaTsc5PMylzDACyLcl8Ry70ihQynlJAMYOz8p0KWoD_fTWly5)

    ![System Context Fiagram](./sample/c4-banking-system.png)

2. Container diagram

    [PlantUml file for diagram below](./sample/c4-banking-container.puml)

    [Edit this diagram online](http://www.plantuml.com/plantuml/uml/bPDHQzim4CVVzIcq3n3xfK-bcD9sq9Lr2qq6WoQKYtsDHQMJa4waO-oxx-mQrtDeMKiVWlZzzB__HJbF396pi-gJeThc1dEqkcKEwRGi8noAlU4sxtB2M7jY92vgxyhqP168MvzJUNcoM5gWxfRLaw7IGMACvIuRsvG-SyXSrYT5w58K6xQeBu24tElqIr2dQWXiFEbrQvAMVsvVaKj91KCODJw32o8pF27fn-ZTE6Xzudo3jXzDAQZPHrtdnDw9TtRsXHWZWTLBZCbJLIbrXpK3xUKw1uOU8pXyU9b6-C_F0x_gJuH_nL5u-nwguiYQFXU97tP3cqu8G0qsLQL_Aor_CdFm7QGFk7k04AofeL_7PF1n2rKrarBukEFypbZy7wyN6s3OGSBnmvI-6iwEGY2OjsxzezIyw-A-DKs3j8rct_AYclLIARoF7rTwEwBn1rfKOnkbngTI59MUQwVwHy8DtLypXxJzbqtX64rJP3hO75FTXeg-W73pPpXG4lppzklcUhrUhhOlXiL74SRn1Rn3Q5B_YzWGKACFqJ0cpLxicwkBo-sGbODuqmSixWf5wCysb9EXlJYhs_LogwRWu8xDffwQVpb5js2X9VErnStg-xTog37kv0FEkUHbP_y2)

    ![Container diagram](./sample/c4-banking-container.png)

3. Component diagram

    ## _**!!!TODO!!!**_

## Brief description
---

This project will help you use the awesome plantuml tool to create C4 diagrams for documenting architecture.

C4 defines a set of diagrams (core and supplamentary) that are designed to document architecture in a way that is easy to understand and communicate.

PlantUml is a uniquely pleasant-to-use tool to create diagrams from text. The fact that this is a text-driven tool opens up a lot of previously impossible scenarios:

1. It is a *pleasure* to edit
1. You don't need special tooling
1. You can keep your domain models side-by-side with your code
1. You can embedd models in your markdown documents in almost all major editors
1. Did I mention that it is an absolute pleasure to work with plantuml?

The only real disadvantage to plantuml is that positioning can sometimes be a bit hard.

This tool allows you to use stereotypes to skin your diagram to be close to what is standard with C4. You can use this include to skin the following diagrams:

1. System Context diagram
1. Container diagram
1. Component diagram
1. System Landscape diagram
1. Dynamic diagram
1. Dynamic diagram

## Instructions
---

All that is needed to start is to add the following line:
```plantumlcode
!includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml
```

> **NOTE**: This will set your diagram type as a deployment diagram. If you want to add some incompatible artifacts in your diagram, please also add the following statement below the `includeurl` one
> ```plantumlcode
> allowmixing
> ```

1. ### Stereotypes and legend

    As mentioned above, the way that you would skin your artifacts is through the use of stereotyping. Due to this, currently stereotype names are not emitted, but instead, a legend is emited on the bottom right. At this time it cannot be turned off.

2. ### Represent C4 Person --> with PlantUml Actors

    There is support for two types of actors. Internal and external actors. The supported stereotypes are:
    - `<<Internal>>`
    - `<<External>>`
    
    The following code:

    ```plantumlcode
    @startuml
    !define NO_LEGEND

    !includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml

    actor Internal <<Internal>>
    actor External <<External>>
    actor InternalPerson <<Internal Person>>
    actor ExternalPerson <<External Person>>

    External -down-> Internal
    Internal -right-> InternalPerson
    InternalPerson -up-> ExternalPerson

    @end
    ```

    Produces this outcome:

    ![Actors](./docs/diagrams/actors.png)

3. #### Represent C4 Systems --> with PlantUml Rectangles and Frames

    C4 Systems can be reprensented using PlantUml rectangles and frames. In both cases the stereotypes that could be used are:

    > **NOTE**: the simplicity of rectangles makes them really useful if you want to avoid the connotations implied by UML artifacts, so they are used to represent other C4 artifacts too

    - `<<Internal System>>`
    - `<<System>>` (an alias to `<<Internal System>>`)
    - `<<External System>>`

    The following code:

    ```plantumlcode
    @startuml
    !define NO_LEGEND

    !includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml

    rectangle Internal <<Internal System>>
    frame AnotherInternal <<System>>
    rectangle External <<External System>>
    frame AnotherExternal <<External System>>

    Internal -right-> External
    Internal -[hidden]down-> AnotherInternal
    AnotherInternal -right-> AnotherExternal

    @enduml
    ```

    Produces the outcome:

    ![Systems](./docs/diagrams/systems.png)

4. #### Represent C4 Containers --> with PlantUml Rectangle and Components

    C4 containers can be repesented by using plantuml rectangles  (and not C4 components which is a bit confusing), which are useful to be shown normally on `System Context`, `Container` and `System Landscape` diagrams. The supported stereotypes are:
    
    - `<<Internal Container>>`
    - `<<Container>>` (an alias to `Internal Container`)
    - `<<External Container>>`

    The following code:

    ```plantumlcode
    @startuml
    !define NO_LEGEND

    !includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml

    component InternalComponent <<Internal Container>>
    component ExternalComponent <<External Container>>

    rectangle InternalRectangle <<Internal Container>>
    rectangle ExternalRectangle <<External Container>>

    InternalComponent -right-> ExternalComponent
    InternalComponent -[hidden]down-> InternalRectangle
    InternalRectangle -right-> ExternalRectangle

    @enduml
    ```

    Produces this outcome:

    ![Containers](./docs/diagrams/containers.png)

5. #### Represent C4 components --> with PlantUml rectangles

    C4 components can currently only be represented by plantuml rectangles. The are only really usesful in `Component` C4 diagrams, but obviously really important. The stereotypes used 

    - `<<Internal Component>>`
    - `<<Component>>` (an alias to `<<Internal Component>>`)
    - `<<External Component>>`

    The following code:

    ```plantumlcode
    @startuml
    !define NO_LEGEND

    !includeurl https://raw.githubusercontent.com/skleanthous/C4-PlantumlSkin/master/build/output/c4.puml

    rectangle Internal <<Internal Component>>
    rectangle External <<External Component>>

    Internal -right-> External

    @enduml
    ```

    Produces this outcome:

    ![Components](./docs/diagrams/components.png)

6. #### More details

    The above should be enough to get you started. For more info please see:

    - [Items definitions](./src/items)
    - [PlantUml files for the sample diagrams](./sample/)
    - [List of all supported artifacts](./docs/diagrams/)

## work outstanding

1. Complete examples
1. Add skinning for C4 Code diagrams 

## Inspiration \ Acknowledgements
---

Basically the only acknowledgement is [C4-PlantUML](https://github.com/RicardoNiepel/C4-PlantUML) from [Ricardo Niepel](https://github.com/RicardoNiepel). This is a very good library to work with C4, but I wanted something much more native to plantuml. Specifically I wanted to be able to work with artifacts native to plantuml (`rectangle`, `queue`, `component`, etc.) instead of the "method"-like means that this library exposes.