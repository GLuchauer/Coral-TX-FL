# Coral-TX-FL
A project looking at how gene flow of coral affects resilience to anthropogenic climate change

# 1. Purpose 

The purpose of this project is to model the ability of a coral population in Florida Keys National Marine Sanctuary (FKNMS) to adapt to habitat as habitat continually changes due to anthropogenic climate change. 

Eventually generation of TX coral will become more adapted to heat resilience 

# 2. Entities, state variables, and scales

#Agents are star coral colonies "Orbicella spp."

colonies come into existence via transplantation from lab specimens, translocation from coral reefs in the Gulf of Mexico and the Carribbean Sea and local reproduction via sexual reproduction and fragementation.

# scale is the coral habitat of FKNMS

The primary focus in FKNMS, with some analysis of the Carribbean marine system, mostly long distance ocean currents

#State variables

Time = years

Population = total number of coral

#Recruits

number of local coral 

number of transplanted coral

number of translocated coral

#Mortality 

number of bleached coral

number of dead coral

death rate due to lack of current resilience - natural boulder coral mortality is very low due to their long lives and colonial nature.

Resilience variable = between 0 and 1. Corals are resilient when their Resilience variable is the same as the current Climate variable - how well acclimated is the current population to the current habitat.

Climate variable = between 0 and 1 and increases over time 
Substrate - determine where colonies successfully develop - based on changing parameters of the habitat. Temperature, pH, chlorophyll-a

#3. Process overview 

corals in FKNMS are under a constant pressure to adapt to increasing water temperatures. In order to maintain colonies, corals that survive heat stress events are taken into captive propagation to produce resilient genotypes, which are planted into the system once colonies are large enough. 

However, FKNMS is not a isolated or closed system. Caribbean organisms move from the Gulf of Mexico and Main Caribbean (Cuba and Dutch Caribbean) to FKNMS. Many of the successful reefs are in deeper, cooler waters which are buffered from heat stress.

For the class project, all translocation will be from Texas and all transplanted coral are offspring of FKNMS resilient coral - no super corals.

#4. Initialization 

In order to build this model, we need to use Resilience and Climate as sliding scales over time. As Climate increases, corals will undergo a mortality event and rebound as the total population adapts to the new conditions. This cycle repeats annually, where summer typically has the mortality event. 

Corals rebound in the fall - spring with sexual reproduction in late summer/early fall and transplantation occurring through the fall-spring. Texas corals will start to arrive several weeks after their spawn in mid-August. 

Produce a graph showing population with respect to time given both the Climate and Resilience sliding scales.

#5. Description of different subroutines/functions/actions that need to happen in the model
we need a smallest survivable colony size - the size that transplanted coral go into the system

a large proportion (95%) of potential translocated coral polyps fail to migrate to FKNMS

As the climate variable increases, the resilience variable will cause a crash (mass mortality) in the system, that will likely require transplants to return to previous percent coral cover. 

Texas corals will have lower Resilience than local and lab corals due to the difference in spawning habitat. However, the Resilience of Texas corals will increase with time.

Assume that transplanted corals have the same Resilience as local corals. - For the final model, transplanted corals will likely have a higher Resilience for temperature. Neutral or less for other parameters.

Potential coral habitat will decrease with time due to erosion and algal invasion, but this will likely be excluded from the class model.

