= Coil Validation Project =

== Introduction ==

The purpose of this project is ensure that we can accurately predict coil performance and maintain AHRI certification.
Component tests of coils will be performed in order to develop methods to accurately predict performance.
These predictions will be used by the sales and application engineers in component selection and by AHRI for the certification of coils.

== Roles ==

 * Charles Rymal
   * Project manager
   * test plan/charter
   * data acquisition request
   * data analysis
   * report
 * Matt Simones
   * test lab manager
   * technical support
   * test procedure support
 * Tony Heald/Pierre Blanchard
   * manufacturing support

== Scope ==

Products include all single phase (water) and evaporator coils produced by NAS.

An end date for the non-recurring phase of the project has yet to be determined.

The project can divided into non-recurring and recurring tasks. The non-recurring phase has three main components: determine what needs to be tested, perform tests, analyze and apply test results.

Schedule

 * Estimate what coils we need to test and individual time
 * Estimate what headers we need to test and individual time

== Goals ==

 * Validate/derive coil performance
   * Calculate coefficients for mathematical models used in sizing and selection software
   * Under AHRI 410 standard conditions for all coil options
   * Outside of AHRI conditions
     * For datacenter market, need to define
     * Coil options
     * 3/8 inch lanced
     * 1/2 inch standard (sine wave with rippled edge)
     * 1/2 inch lanced "3 up"
 * Validate coil header performance
   * Calculate coefficients for new mathematical models
   * Affects system performance through tube-side pressure drop and flow distribution in coil
   * Tube-side pressure drop should be known accurately during design for accurate prediction of performance and for sizing components
 * Validate ongoing quality/performance
   * Test Intertek disposition coils
     * This also validates our test procedure/ compatibility with Intertek
   * Spot test production coils
 * Derive application rules of coils
   * Angle/orientation
     * Slab and Vee
     * Effect on capacity and air-side pressure drop
   * Face velocity limitations
     * Water carry-over
 * New fin die, 1/2 inch lanced "3 up"
   * Compare existing versus new die (spot check)
 * New tube material UNILLOY
 * Variance between manufacturing location (spot check)


== Who is affected by this project? (who is the customer?) ==

 * developers of the software
   * Greg Lanz works on NASDA
   * Yuri Bakshi works on Mammoth Coil Selection
 * users of software that performs coil calculations
   * reps
   * sales and app engineers
   * thermal engineers

== Budget ==

Coming soon: estimate of total project cost. Currently working on the following items needed for this:

 * preliminary test matrices for ALL test coils and ALL test headers
   * estimate of manufacturing cost for each
   * estimate of test duration (setup, data collection, cleanup) for each

== Objectives ==

 * Non-recurring
   * [Software with updated coefficients and calculation methods](deliver/coefficients/index.html)
   * [AHRI certification](deliver/ahri_cert/index.html)
   * Relationship between face velocity and water carryover
   * Relationship between capacity and air pressure drop and air incident angle
   * Comparison between old and new 0.5 inch lanced fin
   * Comparison between manufacturing locations (spot check)
   * Comparison between straight and rippled edge
   * Comparison of third party coils, out coils, and third party rating software
   * new tube material: UNILLOY
   * additional
     * Tony wants to test some 8 row coils with electrofin(?) for water carryover
 * Recurring
   * test coils returned from Intertek
     * Comparison between Intertek and our test results
     * validates out test procedure/compatibility with Intertek
   * spot check test production coils
     * Detect changes in performance over time
   * Detect changes in materials over time that could impact performance
