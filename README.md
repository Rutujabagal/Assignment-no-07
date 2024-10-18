BulkDensity = float(input(“Enter the value of Bulk Density of soil: “))

SatDensity = float(input(“Enter the value of Saturated Density of soil: “))

WaterDensity = float(input(“Enter the unit weight of water: “))

Df = float(input(“Enter the value of depth of footing: “))

Dw = float(input(“Enter the value of water table above footing level: “))

Dw2 = float(input(“Enter the value of water table below the footing level: “))

B = float(input(“Enter the value of width of footing: “))

Nq = float(input(“Enter the value of Nq: “))

Ng = float(input(“Enter the value of N gamma (Ng): “))

# Calculation of Submerged Density of soil

SubDensity = SatDensity – WaterDensity

Print(“Submerged Weight of soil is:”, SubDensity)

# Case A: Water table at ground level

Print(“\nCASE A: Water table at ground level”)

Qu_case_a = (SubDensity * Df) + (0.5 * BulkDensity * B * Ng)

Print(“The value of ultimate bearing capacity of soil for Case A is:”, qu_case_a)

# Approximate calculation of Bearing capacity with water table effects

Rw = 0.5 + 0.5 * (Dw / B)

Print(“The value of Rw is:”, Rw)

Rw1 = 0.5 – 0.15 * (Dw / B)

Print(“The value of Rw1 is:”, Rw1)

# Bearing capacity for the water table effects

Qu_case_b = (BulkDensity * Df * Nq * Rw) + (0.5 * BulkDensity * B * Ng * Rw1)

Print(“The value of ultimate bearing capacity of soil for Case B is:”, qu_case_b)
