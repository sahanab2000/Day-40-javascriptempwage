const IS_PART_TIME = 1;
const IS_FULL_TIME = 2;
const PART_TIME_HOURS = 4;
const FULL_TIME_HOURS = 8;
const WGE_PER_HOURS = 20;
const MAX_HRS_IN_MONTH = 150;
const MAX_DAYS_IN_MONTH = 20;

let empHours =0;
let workingDays = 0;

function getWorkingHours (empCheck)
{
    switch(empCheck)
    {
        case IS_PART_TIME:
            return PART_TIME_HOURS;
        
        case IS_FULL_TIME:
            return FULL_TIME_HOURS;
        
        default:
        return 0;
    }

}

while(empHours <= MAX_HRS_IN_MONTH && workingDays < MAX_DAYS_IN_MONTH)
{
    workingDays++;

    let empCheck = Math.floor(Math.random()*10)%3;

    empHours += getWorkingHours(empCheck);
}


let empWage = empHours * WGE_PER_HOURS;

console.log("Total Working Days are: " + workingDays +" Total working hours: " + empHours + " Employee Monthly Wages is: " +empWage);