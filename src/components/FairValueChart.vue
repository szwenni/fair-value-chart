
<template>
  <div class="flex flew-row w-full">
    <div class="justify-center w-full p-10" id="chartplh"></div>
  </div>
</template>
<script>
import { ref } from "vue";
import ApexCharts from "apexcharts";
export default {
  name: "FairValueChart",
  setup() {
    let fvDataJson =
      /*`[
  {
    "year": 2001,
    "bilIcomePS": 0.83,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 10.265625,
        "priceHigh": 13.875
      },
      {
        "month": 2,
        "priceLow": 10.55,
        "priceHigh": 12.1875
      },
      {
        "month": 3,
        "priceLow": 9.825,
        "priceHigh": 12.675
      },
      {
        "month": 4,
        "priceLow": 9.415,
        "priceHigh": 12.255
      },
      {
        "month": 5,
        "priceLow": 10.2875,
        "priceHigh": 12.465
      },
      {
        "month": 6,
        "priceLow": 8.7275,
        "priceHigh": 11.5175
      },
      {
        "month": 7,
        "priceLow": 7.6875,
        "priceHigh": 9.2475
      },
      {
        "month": 8,
        "priceLow": 7.7525,
        "priceHigh": 9.0725
      },
      {
        "month": 9,
        "priceLow": 6.45,
        "priceHigh": 8.2975
      },
      {
        "month": 10,
        "priceLow": 6.9125,
        "priceHigh": 9.85
      },
      {
        "month": 11,
        "priceLow": 7.625,
        "priceHigh": 9.5
      },
      {
        "month": 12,
        "priceLow": 8.35,
        "priceHigh": 9.915
      }
    ]
  },
  {
    "year": 2002,
    "bilIcomePS": 0.16,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 7.625,
        "priceHigh": 9.6025
      },
      {
        "month": 2,
        "priceLow": 7.79,
        "priceHigh": 8.925
      },
      {
        "month": 3,
        "priceLow": 8.675,
        "priceHigh": 10.33
      },
      {
        "month": 4,
        "priceLow": 9.4325,
        "priceHigh": 10.7375
      },
      {
        "month": 5,
        "priceLow": 10.0975,
        "priceHigh": 11.0375
      },
      {
        "month": 6,
        "priceLow": 9.2775,
        "priceHigh": 10.285
      },
      {
        "month": 7,
        "priceLow": 7.505,
        "priceHigh": 9.92
      },
      {
        "month": 8,
        "priceLow": 7.9675,
        "priceHigh": 9.1
      },
      {
        "month": 9,
        "priceLow": 8.1725,
        "priceHigh": 9.0875
      },
      {
        "month": 10,
        "priceLow": 8.1,
        "priceHigh": 9.8325
      },
      {
        "month": 11,
        "priceLow": 8.83,
        "priceHigh": 10.1825
      },
      {
        "month": 12,
        "priceLow": 9.665,
        "priceHigh": 10.5
      }
    ]
  },
  {
    "year": 2003,
    "bilIcomePS": 0.92,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 8.925,
        "priceHigh": 10.3625
      },
      {
        "month": 2,
        "priceLow": 9.4525,
        "priceHigh": 10.7075
      },
      {
        "month": 3,
        "priceLow": 9.575,
        "priceHigh": 10.7075
      },
      {
        "month": 4,
        "priceLow": 9.14,
        "priceHigh": 10.07
      },
      {
        "month": 5,
        "priceLow": 9.1775,
        "priceHigh": 10.775
      },
      {
        "month": 6,
        "priceLow": 10.1325,
        "priceHigh": 11.39
      },
      {
        "month": 7,
        "priceLow": 9.425,
        "priceHigh": 10.46
      },
      {
        "month": 8,
        "priceLow": 9.4675,
        "priceHigh": 10.61
      },
      {
        "month": 9,
        "priceLow": 10.0725,
        "priceHigh": 10.7175
      },
      {
        "month": 10,
        "priceLow": 10.2125,
        "priceHigh": 10.7375
      },
      {
        "month": 11,
        "priceLow": 10.315,
        "priceHigh": 10.915
      },
      {
        "month": 12,
        "priceLow": 10.4875,
        "priceHigh": 11.88
      }
    ]
  },
  {
    "year": 2004,
    "bilIcomePS": 1.29,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 11.1225,
        "priceHigh": 11.8625
      },
      {
        "month": 2,
        "priceLow": 10.6125,
        "priceHigh": 11.455
      },
      {
        "month": 3,
        "priceLow": 10.82,
        "priceHigh": 11.5725
      },
      {
        "month": 4,
        "priceLow": 11.33,
        "priceHigh": 12.6975
      },
      {
        "month": 5,
        "priceLow": 12.2775,
        "priceHigh": 13.82
      },
      {
        "month": 6,
        "priceLow": 12.9575,
        "priceHigh": 15.9225
      },
      {
        "month": 7,
        "priceLow": 14.825,
        "priceHigh": 15.95
      },
      {
        "month": 8,
        "priceLow": 13.8,
        "priceHigh": 16.525
      },
      {
        "month": 9,
        "priceLow": 14.4375,
        "priceHigh": 16.717501
      },
      {
        "month": 10,
        "priceLow": 16.219999,
        "priceHigh": 18.120001
      },
      {
        "month": 11,
        "priceLow": 16.0375,
        "priceHigh": 19.125
      },
      {
        "month": 12,
        "priceLow": 17.092501,
        "priceHigh": 18.8375
      }
    ]
  },
  {
    "year": 2005,
    "bilIcomePS": 2.57,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 16.025,
        "priceHigh": 18.700001
      },
      {
        "month": 2,
        "priceLow": 18.682501,
        "priceHigh": 23.325001
      },
      {
        "month": 3,
        "priceLow": 21.8675,
        "priceHigh": 24.42
      },
      {
        "month": 4,
        "priceLow": 21.4,
        "priceHigh": 26.25
      },
      {
        "month": 5,
        "priceLow": 21.200001,
        "priceHigh": 25.5
      },
      {
        "month": 6,
        "priceLow": 24.565001,
        "priceHigh": 28.969999
      },
      {
        "month": 7,
        "priceLow": 28.59,
        "priceHigh": 32.939999
      },
      {
        "month": 8,
        "priceLow": 29.375,
        "priceHigh": 32.605
      },
      {
        "month": 9,
        "priceLow": 32.165001,
        "priceHigh": 38.5
      },
      {
        "month": 10,
        "priceLow": 29.98,
        "priceHigh": 39.185001
      },
      {
        "month": 11,
        "priceLow": 31.065001,
        "priceHigh": 36.849998
      },
      {
        "month": 12,
        "priceLow": 35.895,
        "priceHigh": 41
      }
    ]
  },
  {
    "year": 2006,
    "bilIcomePS": 2.62,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 37,
        "priceHigh": 43.16
      },
      {
        "month": 2,
        "priceLow": 32.805,
        "priceHigh": 43.455002
      },
      {
        "month": 3,
        "priceLow": 32.060001,
        "priceHigh": 37.610001
      },
      {
        "month": 4,
        "priceLow": 34.244999,
        "priceHigh": 39.619999
      },
      {
        "month": 5,
        "priceLow": 29.799999,
        "priceHigh": 38.645
      },
      {
        "month": 6,
        "priceLow": 28.155001,
        "priceHigh": 34.990002
      },
      {
        "month": 7,
        "priceLow": 32.150002,
        "priceHigh": 37.779999
      },
      {
        "month": 8,
        "priceLow": 32.064999,
        "priceHigh": 36.825001
      },
      {
        "month": 9,
        "priceLow": 29.225,
        "priceHigh": 33.41
      },
      {
        "month": 10,
        "priceLow": 29.940001,
        "priceHigh": 35.535
      },
      {
        "month": 11,
        "priceLow": 32.290001,
        "priceHigh": 36.134998
      },
      {
        "month": 12,
        "priceLow": 30.934999,
        "priceHigh": 35.360001
      }
    ]
  },
  {
    "year": 2007,
    "bilIcomePS": 2.19,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 29.605,
        "priceHigh": 34.875
      },
      {
        "month": 2,
        "priceLow": 32.200001,
        "priceHigh": 34.974998
      },
      {
        "month": 3,
        "priceLow": 32,
        "priceHigh": 36.544998
      },
      {
        "month": 4,
        "priceLow": 35.575001,
        "priceHigh": 38.855
      },
      {
        "month": 5,
        "priceLow": 36.900002,
        "priceHigh": 39.605
      },
      {
        "month": 6,
        "priceLow": 35.665001,
        "priceHigh": 40.744999
      },
      {
        "month": 7,
        "priceLow": 34.150002,
        "priceHigh": 38.459999
      },
      {
        "month": 8,
        "priceLow": 32.645,
        "priceHigh": 37.915001
      },
      {
        "month": 9,
        "priceLow": 33.43,
        "priceHigh": 37.625
      },
      {
        "month": 10,
        "priceLow": 36.099998,
        "priceHigh": 44.855
      },
      {
        "month": 11,
        "priceLow": 40.395,
        "priceHigh": 45.365002
      },
      {
        "month": 12,
        "priceLow": 40.785,
        "priceHigh": 45.814999
      }
    ]
  },
  {
    "year": 2008,
    "bilIcomePS": 4.86,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 38.59,
        "priceHigh": 47.18
      },
      {
        "month": 2,
        "priceLow": 43.435001,
        "priceHigh": 64.949997
      },
      {
        "month": 3,
        "priceLow": 52.950001,
        "priceHigh": 64.074997
      },
      {
        "month": 4,
        "priceLow": 58.880001,
        "priceHigh": 70.245003
      },
      {
        "month": 5,
        "priceLow": 61.360001,
        "priceHigh": 72.495003
      },
      {
        "month": 6,
        "priceLow": 61.305,
        "priceHigh": 68.625
      },
      {
        "month": 7,
        "priceLow": 49,
        "priceHigh": 66.945
      },
      {
        "month": 8,
        "priceLow": 45.529999,
        "priceHigh": 55.77
      },
      {
        "month": 9,
        "priceLow": 39.900002,
        "priceHigh": 51.110001
      },
      {
        "month": 10,
        "priceLow": 27.209999,
        "priceHigh": 45.400002
      },
      {
        "month": 11,
        "priceLow": 32,
        "priceHigh": 44.439999
      },
      {
        "month": 12,
        "priceLow": 29.945,
        "priceHigh": 41.400002
      }
    ]
  },
  {
    "year": 2009,
    "bilIcomePS": 1.09,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 30.145,
        "priceHigh": 36.415001
      },
      {
        "month": 2,
        "priceLow": 24.43,
        "priceHigh": 35.860001
      },
      {
        "month": 3,
        "priceLow": 22.514999,
        "priceHigh": 33.325001
      },
      {
        "month": 4,
        "priceLow": 26.545,
        "priceHigh": 33.465
      },
      {
        "month": 5,
        "priceLow": 31.639999,
        "priceHigh": 39.560001
      },
      {
        "month": 6,
        "priceLow": 32.849998,
        "priceHigh": 39.255001
      },
      {
        "month": 7,
        "priceLow": 30.145,
        "priceHigh": 37.48
      },
      {
        "month": 8,
        "priceLow": 35.509998,
        "priceHigh": 39.825001
      },
      {
        "month": 9,
        "priceLow": 34.314999,
        "priceHigh": 42.215
      },
      {
        "month": 10,
        "priceLow": 39.685001,
        "priceHigh": 47.93
      },
      {
        "month": 11,
        "priceLow": 40.185001,
        "priceHigh": 46.330002
      },
      {
        "month": 12,
        "priceLow": 42,
        "priceHigh": 50.880001
      }
    ]
  },
  {
    "year": 2010,
    "bilIcomePS": 0.32,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 44.685001,
        "priceHigh": 50.220001
      },
      {
        "month": 2,
        "priceLow": 43.389999,
        "priceHigh": 49.110001
      },
      {
        "month": 3,
        "priceLow": 43.764999,
        "priceHigh": 49.689999
      },
      {
        "month": 4,
        "priceLow": 47.005001,
        "priceHigh": 57.474998
      },
      {
        "month": 5,
        "priceLow": 46.639999,
        "priceHigh": 57.450001
      },
      {
        "month": 6,
        "priceLow": 49.025002,
        "priceHigh": 56.950001
      },
      {
        "month": 7,
        "priceLow": 47.889999,
        "priceHigh": 54.235001
      },
      {
        "month": 8,
        "priceLow": 42.709999,
        "priceHigh": 51.875
      },
      {
        "month": 9,
        "priceLow": 43.634998,
        "priceHigh": 47.424999
      },
      {
        "month": 10,
        "priceLow": 46.830002,
        "priceHigh": 51.029999
      },
      {
        "month": 11,
        "priceLow": 43,
        "priceHigh": 49.18
      },
      {
        "month": 12,
        "priceLow": 44.764999,
        "priceHigh": 48.035
      }
    ]
  },
  {
    "year": 2011,
    "bilIcomePS": 2.05,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 45.419998,
        "priceHigh": 53.290001
      },
      {
        "month": 2,
        "priceLow": 51.169998,
        "priceHigh": 57.584999
      },
      {
        "month": 3,
        "priceLow": 51,
        "priceHigh": 60.720001
      },
      {
        "month": 4,
        "priceLow": 53.919998,
        "priceHigh": 59.91
      },
      {
        "month": 5,
        "priceLow": 50.919998,
        "priceHigh": 56.900002
      },
      {
        "month": 6,
        "priceLow": 48.310001,
        "priceHigh": 56.02
      },
      {
        "month": 7,
        "priceLow": 48.200001,
        "priceHigh": 53.939999
      },
      {
        "month": 8,
        "priceLow": 42.790001,
        "priceHigh": 52.16
      },
      {
        "month": 9,
        "priceLow": 34.775002,
        "priceHigh": 47.080002
      },
      {
        "month": 10,
        "priceLow": 33.404999,
        "priceHigh": 47.630001
      },
      {
        "month": 11,
        "priceLow": 41.939999,
        "priceHigh": 52.235001
      },
      {
        "month": 12,
        "priceLow": 46.505001,
        "priceHigh": 53.099998
      }
    ]
  },
  {
    "year": 2012,
    "bilIcomePS": 1.06,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 49.91,
        "priceHigh": 53.75
      },
      {
        "month": 2,
        "priceLow": 52.34,
        "priceHigh": 59.985001
      },
      {
        "month": 3,
        "priceLow": 53.575001,
        "priceHigh": 58.985001
      },
      {
        "month": 4,
        "priceLow": 50.294998,
        "priceHigh": 57.165001
      },
      {
        "month": 5,
        "priceLow": 47.889999,
        "priceHigh": 56.119999
      },
      {
        "month": 6,
        "priceLow": 41.240002,
        "priceHigh": 48.700001
      },
      {
        "month": 7,
        "priceLow": 43.77,
        "priceHigh": 50.810001
      },
      {
        "month": 8,
        "priceLow": 47.639999,
        "priceHigh": 55.779999
      },
      {
        "month": 9,
        "priceLow": 53.595001,
        "priceHigh": 59.845001
      },
      {
        "month": 10,
        "priceLow": 53.880001,
        "priceHigh": 58.285
      },
      {
        "month": 11,
        "priceLow": 56.360001,
        "priceHigh": 62.244999
      },
      {
        "month": 12,
        "priceLow": 58.285,
        "priceHigh": 62.25
      }
    ]
  },
  {
    "year": 2013,
    "bilIcomePS": 4.02,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 60.720001,
        "priceHigh": 64.714996
      },
      {
        "month": 2,
        "priceLow": 60.380001,
        "priceHigh": 69.099998
      },
      {
        "month": 3,
        "priceLow": 60.5,
        "priceHigh": 66.419998
      },
      {
        "month": 4,
        "priceLow": 56.025002,
        "priceHigh": 65.099998
      },
      {
        "month": 5,
        "priceLow": 58.880001,
        "priceHigh": 69.5
      },
      {
        "month": 6,
        "priceLow": 62.264999,
        "priceHigh": 68.995003
      },
      {
        "month": 7,
        "priceLow": 66.620003,
        "priceHigh": 75.025002
      },
      {
        "month": 8,
        "priceLow": 73.785004,
        "priceHigh": 80.735001
      },
      {
        "month": 9,
        "priceLow": 78.525002,
        "priceHigh": 86.959999
      },
      {
        "month": 10,
        "priceLow": 84.275002,
        "priceHigh": 94.150002
      },
      {
        "month": 11,
        "priceLow": 82.095001,
        "priceHigh": 91.800003
      },
      {
        "month": 12,
        "priceLow": 78.004997,
        "priceHigh": 85.25
      }
    ]
  },
  {
    "year": 2014,
    "bilIcomePS": 5.32,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 80.629997,
        "priceHigh": 86.639999
      },
      {
        "month": 2,
        "priceLow": 80.75,
        "priceHigh": 95.540001
      },
      {
        "month": 3,
        "priceLow": 90.830002,
        "priceHigh": 99.75
      },
      {
        "month": 4,
        "priceLow": 96.529999,
        "priceHigh": 105.5
      },
      {
        "month": 5,
        "priceLow": 96.010002,
        "priceHigh": 106.709999
      },
      {
        "month": 6,
        "priceLow": 104.949997,
        "priceHigh": 118.889999
      },
      {
        "month": 7,
        "priceLow": 109.370003,
        "priceHigh": 118.809998
      },
      {
        "month": 8,
        "priceLow": 103.57,
        "priceHigh": 112.120003
      },
      {
        "month": 9,
        "priceLow": 97.449997,
        "priceHigh": 109.849998
      },
      {
        "month": 10,
        "priceLow": 81.07,
        "priceHigh": 99.730003
      },
      {
        "month": 11,
        "priceLow": 85.190002,
        "priceHigh": 103.040001
      },
      {
        "month": 12,
        "priceLow": 83.660004,
        "priceHigh": 97.269997
      }
    ]
  },
  {
    "year": 2015,
    "bilIcomePS": -8.29,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 82.720001,
        "priceHigh": 94.410004
      },
      {
        "month": 2,
        "priceLow": 86.580002,
        "priceHigh": 97.879997
      },
      {
        "month": 3,
        "priceLow": 84.099998,
        "priceHigh": 92.5
      },
      {
        "month": 4,
        "priceLow": 89.230003,
        "priceHigh": 100.440002
      },
      {
        "month": 5,
        "priceLow": 88,
        "priceHigh": 101.360001
      },
      {
        "month": 6,
        "priceLow": 86.150002,
        "priceHigh": 91.480003
      },
      {
        "month": 7,
        "priceLow": 72.860001,
        "priceHigh": 87.849998
      },
      {
        "month": 8,
        "priceLow": 68.150002,
        "priceHigh": 80.879997
      },
      {
        "month": 9,
        "priceLow": 69.099998,
        "priceHigh": 81.18
      },
      {
        "month": 10,
        "priceLow": 71.589996,
        "priceHigh": 88.300003
      },
      {
        "month": 11,
        "priceLow": 80.5,
        "priceHigh": 89.519997
      },
      {
        "month": 12,
        "priceLow": 69.300003,
        "priceHigh": 84.129997
      }
    ]
  },
  {
    "year": 2016,
    "bilIcomePS": -1.98,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 57.150002,
        "priceHigh": 71.18
      },
      {
        "month": 2,
        "priceLow": 63.060001,
        "priceHigh": 72.769997
      },
      {
        "month": 3,
        "priceLow": 62.529999,
        "priceHigh": 77.699997
      },
      {
        "month": 4,
        "priceLow": 69.660004,
        "priceHigh": 85.43
      },
      {
        "month": 5,
        "priceLow": 77.040001,
        "priceHigh": 83.940002
      },
      {
        "month": 6,
        "priceLow": 78.110001,
        "priceHigh": 86.870003
      },
      {
        "month": 7,
        "priceLow": 78.040001,
        "priceHigh": 85.959999
      },
      {
        "month": 8,
        "priceLow": 78.260002,
        "priceHigh": 92.099998
      },
      {
        "month": 9,
        "priceLow": 87.18,
        "priceHigh": 97.199997
      },
      {
        "month": 10,
        "priceLow": 90.18,
        "priceHigh": 98.32
      },
      {
        "month": 11,
        "priceLow": 88.940002,
        "priceHigh": 103.07
      },
      {
        "month": 12,
        "priceLow": 100.540001,
        "priceHigh": 109.370003
      }
    ]
  },
  {
    "year": 2017,
    "bilIcomePS": 4.46,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 99.57,
        "priceHigh": 106.790001
      },
      {
        "month": 2,
        "priceLow": 95.269997,
        "priceHigh": 102.629997
      },
      {
        "month": 3,
        "priceLow": 92.910004,
        "priceHigh": 100.540001
      },
      {
        "month": 4,
        "priceLow": 91.160004,
        "priceHigh": 100.529999
      },
      {
        "month": 5,
        "priceLow": 88.199997,
        "priceHigh": 96.650002
      },
      {
        "month": 6,
        "priceLow": 85.879997,
        "priceHigh": 91.980003
      },
      {
        "month": 7,
        "priceLow": 87.040001,
        "priceHigh": 96.900002
      },
      {
        "month": 8,
        "priceLow": 81.989998,
        "priceHigh": 95.580002
      },
      {
        "month": 9,
        "priceLow": 84.589996,
        "priceHigh": 98.370003
      },
      {
        "month": 10,
        "priceLow": 94.870003,
        "priceHigh": 100.410004
      },
      {
        "month": 11,
        "priceLow": 96.709999,
        "priceHigh": 107.949997
      },
      {
        "month": 12,
        "priceLow": 98.470001,
        "priceHigh": 109.660004
      }
    ]
  },
  {
    "year": 2018,
    "bilIcomePS": 5.89,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 108.220001,
        "priceHigh": 119
      },
      {
        "month": 2,
        "priceLow": 96.540001,
        "priceHigh": 116.57
      },
      {
        "month": 3,
        "priceLow": 97.440002,
        "priceHigh": 107.910004
      },
      {
        "month": 4,
        "priceLow": 98.800003,
        "priceHigh": 119.709999
      },
      {
        "month": 5,
        "priceLow": 111.480003,
        "priceHigh": 128.029999
      },
      {
        "month": 6,
        "priceLow": 113.93,
        "priceHigh": 126.32
      },
      {
        "month": 7,
        "priceLow": 121.110001,
        "priceHigh": 131.600006
      },
      {
        "month": 8,
        "priceLow": 114.050003,
        "priceHigh": 128.550003
      },
      {
        "month": 9,
        "priceLow": 113.699997,
        "priceHigh": 129.089996
      },
      {
        "month": 10,
        "priceLow": 100.629997,
        "priceHigh": 133.529999
      },
      {
        "month": 11,
        "priceLow": 96.809998,
        "priceHigh": 110.199997
      },
      {
        "month": 12,
        "priceLow": 82.040001,
        "priceHigh": 108.779999
      }
    ]
  },
  {
    "year": 2019,
    "bilIcomePS": 4.71,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 85.199997,
        "priceHigh": 101.370003
      },
      {
        "month": 2,
        "priceLow": 89.940002,
        "priceHigh": 100.489998
      },
      {
        "month": 3,
        "priceLow": 86.139999,
        "priceHigh": 97.629997
      },
      {
        "month": 4,
        "priceLow": 92.919998,
        "priceHigh": 107.889999
      },
      {
        "month": 5,
        "priceLow": 81.830002,
        "priceHigh": 96.5
      },
      {
        "month": 6,
        "priceLow": 80.410004,
        "priceHigh": 94.379997
      },
      {
        "month": 7,
        "priceLow": 82.010002,
        "priceHigh": 95.290001
      },
      {
        "month": 8,
        "priceLow": 70.830002,
        "priceHigh": 87.839996
      },
      {
        "month": 9,
        "priceLow": 72.389999,
        "priceHigh": 87
      },
      {
        "month": 10,
        "priceLow": 64.330002,
        "priceHigh": 74.790001
      },
      {
        "month": 11,
        "priceLow": 69.639999,
        "priceHigh": 75.599998
      },
      {
        "month": 12,
        "priceLow": 68.080002,
        "priceHigh": 84.690002
      }
    ]
  },
  {
    "year": 2020,
    "bilIcomePS": -1.04,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 72.510002,
        "priceHigh": 89.540001
      },
      {
        "month": 2,
        "priceLow": 56.34,
        "priceHigh": 77.980003
      },
      {
        "month": 3,
        "priceLow": 27,
        "priceHigh": 65.410004
      },
      {
        "month": 4,
        "priceLow": 33.549999,
        "priceHigh": 49.110001
      },
      {
        "month": 5,
        "priceLow": 43.259998,
        "priceHigh": 54.369999
      },
      {
        "month": 6,
        "priceLow": 48.009998,
        "priceHigh": 62.43
      },
      {
        "month": 7,
        "priceLow": 44.040001,
        "priceHigh": 52.09
      },
      {
        "month": 8,
        "priceLow": 42.98,
        "priceHigh": 52.779999
      },
      {
        "month": 9,
        "priceLow": 34.900002,
        "priceHigh": 45.380001
      },
      {
        "month": 10,
        "priceLow": 31.219999,
        "priceHigh": 40.150002
      },
      {
        "month": 11,
        "priceLow": 33.400002,
        "priceHigh": 54.779999
      },
      {
        "month": 12,
        "priceLow": 46.310001,
        "priceHigh": 55.950001
      }
    ]
  },
  {
    "year": 2021,
    "bilIcomePS": 5.17,
    "dividend": 0,
    "prices": [
      {
        "month": 1,
        "priceLow": 48.599998,
        "priceHigh": 63.029999
      },
      {
        "month": 2,
        "priceLow": 50.080002,
        "priceHigh": 72.860001
      },
      {
        "month": 3,
        "priceLow": 63.950001,
        "priceHigh": 77.150002
      },
      {
        "month": 4,
        "priceLow": 67.129997,
        "priceHigh": 77.050003
      },
      {
        "month": 5,
        "priceLow": 74.150002,
        "priceHigh": 86.599998
      },
      {
        "month": 6,
        "priceLow": 78.800003,
        "priceHigh": 87.989998
      },
      {
        "month": 7,
        "priceLow": 69.300003,
        "priceHigh": 86.379997
      },
      {
        "month": 8,
        "priceLow": 62.810001,
        "priceHigh": 74.389999
      },
      {
        "month": 9,
        "priceLow": 66.050003,
        "priceHigh": 83.599998
      },
      {
        "month": 10,
        "priceLow": 81.010002,
        "priceHigh": 95.639999
      },
      {
        "month": 11,
        "priceLow": 85.32,
        "priceHigh": 98.199997
      }
    ]
  }
]         
      `*/
      `[
  {
    "year": 2001,
    "bilIcomePS": 1.79,
    "dividend": 1.2,
    "prices": [
      {
        "month": 2,
        "priceLow": 53.799999,
        "priceHigh": 57.700001
      },
      {
        "month": 3,
        "priceLow": 49.25,
        "priceHigh": 59.875
      },
      {
        "month": 4,
        "priceLow": 48.580002,
        "priceHigh": 60.959999
      },
      {
        "month": 5,
        "priceLow": 57.674999,
        "priceHigh": 63.5
      },
      {
        "month": 6,
        "priceLow": 57,
        "priceHigh": 62
      },
      {
        "month": 7,
        "priceLow": 53.389999,
        "priceHigh": 58.75
      },
      {
        "month": 8,
        "priceLow": 51.549999,
        "priceHigh": 56.25
      },
      {
        "month": 9,
        "priceLow": 42.93,
        "priceHigh": 53.794998
      },
      {
        "month": 10,
        "priceLow": 47.599998,
        "priceHigh": 55
      },
      {
        "month": 11,
        "priceLow": 51.700001,
        "priceHigh": 58.845001
      },
      {
        "month": 12,
        "priceLow": 56.349998,
        "priceHigh": 60.950001
      }
    ]
  },
  {
    "year": 2002,
    "bilIcomePS": 2.50,
    "dividend": 1.24,
    "prices": [
      {
        "month": 1,
        "priceLow": 50,
        "priceHigh": 58.994999
      },
      {
        "month": 2,
        "priceLow": 54,
        "priceHigh": 60.400002
      },
      {
        "month": 3,
        "priceLow": 56.450001,
        "priceHigh": 61.849998
      },
      {
        "month": 4,
        "priceLow": 56.150002,
        "priceHigh": 64.050003
      },
      {
        "month": 5,
        "priceLow": 61.5,
        "priceHigh": 65.300003
      },
      {
        "month": 6,
        "priceLow": 59.689999,
        "priceHigh": 64.800003
      },
      {
        "month": 7,
        "priceLow": 54.099998,
        "priceHigh": 65.044998
      },
      {
        "month": 8,
        "priceLow": 58.25,
        "priceHigh": 64.739998
      },
      {
        "month": 9,
        "priceLow": 54.224998,
        "priceHigh": 63.575001
      },
      {
        "month": 10,
        "priceLow": 55.375,
        "priceHigh": 64.900002
      },
      {
        "month": 11,
        "priceLow": 62.700001,
        "priceHigh": 65.775002
      },
      {
        "month": 12,
        "priceLow": 59.990002,
        "priceHigh": 65.239998
      }
    ]
  },
  {
    "year": 2003,
    "bilIcomePS": 3.02,
    "dividend": 1.32,
    "prices": [
      {
        "month": 1,
        "priceLow": 61.525002,
        "priceHigh": 64.57
      },
      {
        "month": 2,
        "priceLow": 60.125,
        "priceHigh": 63.744999
      },
      {
        "month": 3,
        "priceLow": 59.73,
        "priceHigh": 67.474998
      },
      {
        "month": 4,
        "priceLow": 61.294998,
        "priceHigh": 68.375
      },
      {
        "month": 5,
        "priceLow": 60.255001,
        "priceHigh": 63.369999
      },
      {
        "month": 6,
        "priceLow": 62.25,
        "priceHigh": 66.949997
      },
      {
        "month": 7,
        "priceLow": 63.400002,
        "priceHigh": 70.82
      },
      {
        "month": 8,
        "priceLow": 68.885002,
        "priceHigh": 72.849998
      },
      {
        "month": 9,
        "priceLow": 68.154999,
        "priceHigh": 72.175003
      },
      {
        "month": 10,
        "priceLow": 69.800003,
        "priceHigh": 79.300003
      },
      {
        "month": 11,
        "priceLow": 76,
        "priceHigh": 80.160004
      },
      {
        "month": 12,
        "priceLow": 79.400002,
        "priceHigh": 85.400002
      }
    ]
  },
  {
    "year": 2004,
    "bilIcomePS": 3.75,
    "dividend": 1.44,
    "prices": [
      {
        "month": 1,
        "priceLow": 78.410004,
        "priceHigh": 86.199997
      },
      {
        "month": 2,
        "priceLow": 77.57,
        "priceHigh": 81.459999
      },
      {
        "month": 3,
        "priceLow": 74.349998,
        "priceHigh": 81.980003
      },
      {
        "month": 4,
        "priceLow": 80.900002,
        "priceHigh": 88.699997
      },
      {
        "month": 5,
        "priceLow": 81.669998,
        "priceHigh": 87.650002
      },
      {
        "month": 6,
        "priceLow": 84.010002,
        "priceHigh": 90.290001
      },
      {
        "month": 7,
        "priceLow": 80.75,
        "priceHigh": 90.110001
      },
      {
        "month": 8,
        "priceLow": 77.199997,
        "priceHigh": 83.849998
      },
      {
        "month": 9,
        "priceLow": 77.690002,
        "priceHigh": 84.959999
      },
      {
        "month": 10,
        "priceLow": 73.309998,
        "priceHigh": 81.970001
      },
      {
        "month": 11,
        "priceLow": 75.059998,
        "priceHigh": 82.900002
      },
      {
        "month": 12,
        "priceLow": 78.129997,
        "priceHigh": 83.029999
      }
    ]
  },
  {
    "year": 2005,
    "bilIcomePS": 4.16,
    "dividend": 1.68,
    "prices": [
      {
        "month": 1,
        "priceLow": 80.730003,
        "priceHigh": 85.5
      },
      {
        "month": 2,
        "priceLow": 82.949997,
        "priceHigh": 86.980003
      },
      {
        "month": 3,
        "priceLow": 83.519997,
        "priceHigh": 87.449997
      },
      {
        "month": 4,
        "priceLow": 74.949997,
        "priceHigh": 86.209999
      },
      {
        "month": 5,
        "priceLow": 75.089996,
        "priceHigh": 79.230003
      },
      {
        "month": 6,
        "priceLow": 72.25,
        "priceHigh": 78.550003
      },
      {
        "month": 7,
        "priceLow": 71.029999,
        "priceHigh": 76.739998
      },
      {
        "month": 8,
        "priceLow": 70.410004,
        "priceHigh": 75.489998
      },
      {
        "month": 9,
        "priceLow": 70.610001,
        "priceHigh": 74.580002
      },
      {
        "month": 10,
        "priceLow": 69.709999,
        "priceHigh": 76.480003
      },
      {
        "month": 11,
        "priceLow": 74.400002,
        "priceHigh": 79.379997
      },
      {
        "month": 12,
        "priceLow": 73.470001,
        "priceHigh": 79.839996
      }
    ]
  },
  {
    "year": 2006,
    "bilIcomePS": 5.06,
    "dividend": 1.84,
    "prices": [
      {
        "month": 1,
        "priceLow": 71.959999,
        "priceHigh": 79.830002
      },
      {
        "month": 2,
        "priceLow": 70.300003,
        "priceHigh": 74.660004
      },
      {
        "month": 3,
        "priceLow": 71.540001,
        "priceHigh": 78.739998
      },
      {
        "month": 4,
        "priceLow": 75.760002,
        "priceHigh": 85.900002
      },
      {
        "month": 5,
        "priceLow": 82.589996,
        "priceHigh": 88.349998
      },
      {
        "month": 6,
        "priceLow": 78.610001,
        "priceHigh": 85.230003
      },
      {
        "month": 7,
        "priceLow": 67.050003,
        "priceHigh": 81.599998
      },
      {
        "month": 8,
        "priceLow": 68.18,
        "priceHigh": 72
      },
      {
        "month": 9,
        "priceLow": 70.589996,
        "priceHigh": 75.370003
      },
      {
        "month": 10,
        "priceLow": 73,
        "priceHigh": 80.879997
      },
      {
        "month": 11,
        "priceLow": 78.120003,
        "priceHigh": 81.949997
      },
      {
        "month": 12,
        "priceLow": 77.349998,
        "priceHigh": 81.550003
      }
    ]
  },
  {
    "year": 2007,
    "bilIcomePS": 5.60,
    "dividend": 1.92,
    "prices": [
      {
        "month": 1,
        "priceLow": 73.089996,
        "priceHigh": 79.879997
      },
      {
        "month": 2,
        "priceLow": 73.519997,
        "priceHigh": 77.43
      },
      {
        "month": 3,
        "priceLow": 72.900002,
        "priceHigh": 78.160004
      },
      {
        "month": 4,
        "priceLow": 75.910004,
        "priceHigh": 83.25
      },
      {
        "month": 5,
        "priceLow": 82.160004,
        "priceHigh": 89.029999
      },
      {
        "month": 6,
        "priceLow": 84.400002,
        "priceHigh": 88.489998
      },
      {
        "month": 7,
        "priceLow": 87.07,
        "priceHigh": 92.32
      },
      {
        "month": 8,
        "priceLow": 83.209999,
        "priceHigh": 91.510002
      },
      {
        "month": 9,
        "priceLow": 87.209999,
        "priceHigh": 93.980003
      },
      {
        "month": 10,
        "priceLow": 84.080002,
        "priceHigh": 97
      },
      {
        "month": 11,
        "priceLow": 78.980003,
        "priceHigh": 86.279999
      },
      {
        "month": 12,
        "priceLow": 81.599998,
        "priceHigh": 88.699997
      }
    ]
  },
  {
    "year": 2008,
    "bilIcomePS": 4.89,
    "dividend": 2,
    "prices": [
      {
        "month": 1,
        "priceLow": 72.050003,
        "priceHigh": 84.760002
      },
      {
        "month": 2,
        "priceLow": 77.82,
        "priceHigh": 81.650002
      },
      {
        "month": 3,
        "priceLow": 75.239998,
        "priceHigh": 81.68
      },
      {
        "month": 4,
        "priceLow": 76.459999,
        "priceHigh": 83.220001
      },
      {
        "month": 5,
        "priceLow": 75.5,
        "priceHigh": 79.889999
      },
      {
        "month": 6,
        "priceLow": 68.610001,
        "priceHigh": 77.610001
      },
      {
        "month": 7,
        "priceLow": 67.260002,
        "priceHigh": 72.769997
      },
      {
        "month": 8,
        "priceLow": 69.349998,
        "priceHigh": 74.68
      },
      {
        "month": 9,
        "priceLow": 65.510002,
        "priceHigh": 74.709999
      },
      {
        "month": 10,
        "priceLow": 50.009998,
        "priceHigh": 68.309998
      },
      {
        "month": 11,
        "priceLow": 56.25,
        "priceHigh": 67.470001
      },
      {
        "month": 12,
        "priceLow": 53.59,
        "priceHigh": 66.25
      }
    ]
  },
  {
    "year": 2009,
    "bilIcomePS": 4.52,
    "dividend": 2.04,
    "prices": [
      {
        "month": 1,
        "priceLow": 52.310001,
        "priceHigh": 59.810001
      },
      {
        "month": 2,
        "priceLow": 45.169998,
        "priceHigh": 54.66
      },
      {
        "month": 3,
        "priceLow": 40.869999,
        "priceHigh": 51.130001
      },
      {
        "month": 4,
        "priceLow": 48.720001,
        "priceHigh": 58.98
      },
      {
        "month": 5,
        "priceLow": 55.23,
        "priceHigh": 60.23
      },
      {
        "month": 6,
        "priceLow": 56.610001,
        "priceHigh": 61.459999
      },
      {
        "month": 7,
        "priceLow": 57.810001,
        "priceHigh": 71.389999
      },
      {
        "month": 8,
        "priceLow": 69.260002,
        "priceHigh": 73.5
      },
      {
        "month": 9,
        "priceLow": 69.889999,
        "priceHigh": 76
      },
      {
        "month": 10,
        "priceLow": 71.620003,
        "priceHigh": 79.25
      },
      {
        "month": 11,
        "priceLow": 73.349998,
        "priceHigh": 79
      },
      {
        "month": 12,
        "priceLow": 76,
        "priceHigh": 84.32
      }
    ]
  },
  {
    "year": 2010,
    "bilIcomePS": 5.63,
    "dividend": 2.1,
    "prices": [
      {
        "month": 1,
        "priceLow": 79.110001,
        "priceHigh": 85.169998
      },
      {
        "month": 2,
        "priceLow": 77.25,
        "priceHigh": 81.760002
      },
      {
        "month": 3,
        "priceLow": 80.349998,
        "priceHigh": 84.5
      },
      {
        "month": 4,
        "priceLow": 82.690002,
        "priceHigh": 90.25
      },
      {
        "month": 5,
        "priceLow": 68.959999,
        "priceHigh": 90.519997
      },
      {
        "month": 6,
        "priceLow": 72.720001,
        "priceHigh": 83
      },
      {
        "month": 7,
        "priceLow": 77.040001,
        "priceHigh": 87.480003
      },
      {
        "month": 8,
        "priceLow": 78.400002,
        "priceHigh": 88.379997
      },
      {
        "month": 9,
        "priceLow": 79.290001,
        "priceHigh": 88
      },
      {
        "month": 10,
        "priceLow": 83.800003,
        "priceHigh": 91.489998
      },
      {
        "month": 11,
        "priceLow": 83,
        "priceHigh": 87.870003
      },
      {
        "month": 12,
        "priceLow": 83.230003,
        "priceHigh": 87.82
      }
    ]
  },
  {
    "year": 2011,
    "bilIcomePS": 5.96,
    "dividend": 2.2,
    "prices": [
      {
        "month": 1,
        "priceLow": 85.629997,
        "priceHigh": 90.5
      },
      {
        "month": 2,
        "priceLow": 87.440002,
        "priceHigh": 93.650002
      },
      {
        "month": 3,
        "priceLow": 86.910004,
        "priceHigh": 94.160004
      },
      {
        "month": 4,
        "priceLow": 90.580002,
        "priceHigh": 97.5
      },
      {
        "month": 5,
        "priceLow": 91.379997,
        "priceHigh": 97.949997
      },
      {
        "month": 6,
        "priceLow": 90.190002,
        "priceHigh": 95.059998
      },
      {
        "month": 7,
        "priceLow": 86.599998,
        "priceHigh": 98.190002
      },
      {
        "month": 8,
        "priceLow": 76.5,
        "priceHigh": 88.169998
      },
      {
        "month": 9,
        "priceLow": 71.709999,
        "priceHigh": 83.949997
      },
      {
        "month": 10,
        "priceLow": 68.629997,
        "priceHigh": 82.400002
      },
      {
        "month": 11,
        "priceLow": 75.489998,
        "priceHigh": 83.099998
      },
      {
        "month": 12,
        "priceLow": 77.510002,
        "priceHigh": 82.800003
      }
    ]
  },
  {
    "year": 2012,
    "bilIcomePS": 6.32,
    "dividend": 2.36,
    "prices": [
      {
        "month": 1,
        "priceLow": 82.699997,
        "priceHigh": 87.989998
      },
      {
        "month": 2,
        "priceLow": 86.690002,
        "priceHigh": 88.459999
      },
      {
        "month": 3,
        "priceLow": 84.830002,
        "priceHigh": 90
      },
      {
        "month": 4,
        "priceLow": 84.440002,
        "priceHigh": 89.75
      },
      {
        "month": 5,
        "priceLow": 82.949997,
        "priceHigh": 89.949997
      },
      {
        "month": 6,
        "priceLow": 81.989998,
        "priceHigh": 89.599998
      },
      {
        "month": 7,
        "priceLow": 85.339996,
        "priceHigh": 92.080002
      },
      {
        "month": 8,
        "priceLow": 89.230003,
        "priceHigh": 94.300003
      },
      {
        "month": 9,
        "priceLow": 90.459999,
        "priceHigh": 94.099998
      },
      {
        "month": 10,
        "priceLow": 87.410004,
        "priceHigh": 95.459999
      },
      {
        "month": 11,
        "priceLow": 86.739998,
        "priceHigh": 91.970001
      },
      {
        "month": 12,
        "priceLow": 89.599998,
        "priceHigh": 94.139999
      }
    ]
  },
  {
    "year": 2013,
    "bilIcomePS": 6.72,
    "dividend": 2.54,
    "prices": [
      {
        "month": 1,
        "priceLow": 93.959999,
        "priceHigh": 101.949997
      },
      {
        "month": 2,
        "priceLow": 100.580002,
        "priceHigh": 104.559998
      },
      {
        "month": 3,
        "priceLow": 102.589996,
        "priceHigh": 106.879997
      },
      {
        "month": 4,
        "priceLow": 102.889999,
        "priceHigh": 108.720001
      },
      {
        "month": 5,
        "priceLow": 104.419998,
        "priceHigh": 112.379997
      },
      {
        "month": 6,
        "priceLow": 107.150002,
        "priceHigh": 113.25
      },
      {
        "month": 7,
        "priceLow": 108.209999,
        "priceHigh": 118.599998
      },
      {
        "month": 8,
        "priceLow": 112.360001,
        "priceHigh": 119.260002
      },
      {
        "month": 9,
        "priceLow": 112.849998,
        "priceHigh": 122.269997
      },
      {
        "month": 10,
        "priceLow": 116.650002,
        "priceHigh": 126.379997
      },
      {
        "month": 11,
        "priceLow": 124.860001,
        "priceHigh": 134.160004
      },
      {
        "month": 12,
        "priceLow": 125.150002,
        "priceHigh": 140.429993
      }
    ]
  },
  {
    "year": 2014,
    "bilIcomePS": 7.49,
    "dividend": 3.42,
    "prices": [
      {
        "month": 1,
        "priceLow": 126.419998,
        "priceHigh": 139.289993
      },
      {
        "month": 2,
        "priceLow": 123.610001,
        "priceHigh": 135.199997
      },
      {
        "month": 3,
        "priceLow": 129.699997,
        "priceHigh": 135.869995
      },
      {
        "month": 4,
        "priceLow": 132.020004,
        "priceHigh": 139.520004
      },
      {
        "month": 5,
        "priceLow": 138.649994,
        "priceHigh": 143.369995
      },
      {
        "month": 6,
        "priceLow": 141.610001,
        "priceHigh": 145.529999
      },
      {
        "month": 7,
        "priceLow": 140.600006,
        "priceHigh": 146.429993
      },
      {
        "month": 8,
        "priceLow": 138.429993,
        "priceHigh": 145.389999
      },
      {
        "month": 9,
        "priceLow": 140.660004,
        "priceHigh": 147.869995
      },
      {
        "month": 10,
        "priceLow": 130.600006,
        "priceHigh": 154.440002
      },
      {
        "month": 11,
        "priceLow": 152.979996,
        "priceHigh": 160.860001
      },
      {
        "month": 12,
        "priceLow": 155.589996,
        "priceHigh": 168.160004
      }
    ]
  },
  {
    "year": 2015,
    "bilIcomePS": 7.58,
    "dividend": 4.1,
    "prices": [
      {
        "month": 1,
        "priceLow": 157.740005,
        "priceHigh": 166.570007
      },
      {
        "month": 2,
        "priceLow": 160.889999,
        "priceHigh": 169.979996
      },
      {
        "month": 3,
        "priceLow": 161.210007,
        "priceHigh": 170.5
      },
      {
        "month": 4,
        "priceLow": 156.009995,
        "priceHigh": 167.699997
      },
      {
        "month": 5,
        "priceLow": 156.550003,
        "priceHigh": 163.770004
      },
      {
        "month": 6,
        "priceLow": 153.919998,
        "priceHigh": 160.869995
      },
      {
        "month": 7,
        "priceLow": 147.699997,
        "priceHigh": 157.940002
      },
      {
        "month": 8,
        "priceLow": 134,
        "priceHigh": 153.240005
      },
      {
        "month": 9,
        "priceLow": 135.389999,
        "priceHigh": 145.550003
      },
      {
        "month": 10,
        "priceLow": 138.570007,
        "priceHigh": 158.679993
      },
      {
        "month": 11,
        "priceLow": 155.600006,
        "priceHigh": 160.089996
      },
      {
        "month": 12,
        "priceLow": 146.690002,
        "priceHigh": 158.690002
      }
    ]
  },
  {
    "year": 2016,
    "bilIcomePS": 8.16,
    "dividend": 4.44,
    "prices": [
      {
        "month": 1,
        "priceLow": 134.639999,
        "priceHigh": 151
      },
      {
        "month": 2,
        "priceLow": 146.050003,
        "priceHigh": 159.5
      },
      {
        "month": 3,
        "priceLow": 157.610001,
        "priceHigh": 167.5
      },
      {
        "month": 4,
        "priceLow": 164.649994,
        "priceHigh": 170.770004
      },
      {
        "month": 5,
        "priceLow": 163.169998,
        "priceHigh": 171.270004
      },
      {
        "month": 6,
        "priceLow": 165.160004,
        "priceHigh": 175.139999
      },
      {
        "month": 7,
        "priceLow": 173.509995,
        "priceHigh": 182.270004
      },
      {
        "month": 8,
        "priceLow": 177.080002,
        "priceHigh": 181.470001
      },
      {
        "month": 9,
        "priceLow": 174.389999,
        "priceHigh": 181.660004
      },
      {
        "month": 10,
        "priceLow": 165.110001,
        "priceHigh": 175.949997
      },
      {
        "month": 11,
        "priceLow": 163.850006,
        "priceHigh": 175.509995
      },
      {
        "month": 12,
        "priceLow": 171.089996,
        "priceHigh": 180.059998
      }
    ]
  },
  {
    "year": 2017,
    "bilIcomePS": 9.18,
    "dividend": 4.7,
    "prices": [
      {
        "month": 1,
        "priceLow": 173.809998,
        "priceHigh": 180
      },
      {
        "month": 2,
        "priceLow": 173.550003,
        "priceHigh": 188.410004
      },
      {
        "month": 3,
        "priceLow": 188.009995,
        "priceHigh": 193.5
      },
      {
        "month": 4,
        "priceLow": 188.619995,
        "priceHigh": 197.119995
      },
      {
        "month": 5,
        "priceLow": 193.539993,
        "priceHigh": 204.470001
      },
      {
        "month": 6,
        "priceLow": 203.679993,
        "priceHigh": 214.570007
      },
      {
        "month": 7,
        "priceLow": 197.169998,
        "priceHigh": 213.410004
      },
      {
        "month": 8,
        "priceLow": 201.330002,
        "priceHigh": 208.630005
      },
      {
        "month": 9,
        "priceLow": 200.509995,
        "priceHigh": 214.649994
      },
      {
        "month": 10,
        "priceLow": 210.029999,
        "priceHigh": 238.899994
      },
      {
        "month": 11,
        "priceLow": 226.039993,
        "priceHigh": 243.449997
      },
      {
        "month": 12,
        "priceLow": 234.279999,
        "priceHigh": 244.229996
      }
    ]
  },
  {
    "year": 2018,
    "bilIcomePS": 9.27,
    "dividend": 5.44,
    "prices": [
      {
        "month": 1,
        "priceLow": 232.809998,
        "priceHigh": 259.769989
      },
      {
        "month": 2,
        "priceLow": 218.179993,
        "priceHigh": 250.089996
      },
      {
        "month": 3,
        "priceLow": 214.729996,
        "priceHigh": 243.100006
      },
      {
        "month": 4,
        "priceLow": 194.179993,
        "priceHigh": 221.690002
      },
      {
        "month": 5,
        "priceLow": 191.440002,
        "priceHigh": 206.039993
      },
      {
        "month": 6,
        "priceLow": 193.639999,
        "priceHigh": 206.789993
      },
      {
        "month": 7,
        "priceLow": 190.570007,
        "priceHigh": 212.779999
      },
      {
        "month": 8,
        "priceLow": 197.110001,
        "priceHigh": 211.720001
      },
      {
        "month": 9,
        "priceLow": 205.899994,
        "priceHigh": 217.869995
      },
      {
        "month": 10,
        "priceLow": 181.979996,
        "priceHigh": 217.339996
      },
      {
        "month": 11,
        "priceLow": 190.089996,
        "priceHigh": 209.770004
      },
      {
        "month": 12,
        "priceLow": 176.869995,
        "priceHigh": 211.949997
      }
    ]
  },
  {
    "year": 2019,
    "bilIcomePS":7.81,
    "dividend": 5.76,
    "prices": [
      {
        "month": 1,
        "priceLow": 182.889999,
        "priceHigh": 200.889999
      },
      {
        "month": 2,
        "priceLow": 196.25,
        "priceHigh": 211.589996
      },
      {
        "month": 3,
        "priceLow": 198,
        "priceHigh": 210.539993
      },
      {
        "month": 4,
        "priceLow": 186.550003,
        "priceHigh": 219.75
      },
      {
        "month": 5,
        "priceLow": 159.630005,
        "priceHigh": 189.710007
      },
      {
        "month": 6,
        "priceLow": 159.320007,
        "priceHigh": 174.559998
      },
      {
        "month": 7,
        "priceLow": 164.289993,
        "priceHigh": 187.720001
      },
      {
        "month": 8,
        "priceLow": 154,
        "priceHigh": 177.669998
      },
      {
        "month": 9,
        "priceLow": 157.259995,
        "priceHigh": 172.479996
      },
      {
        "month": 10,
        "priceLow": 150.580002,
        "priceHigh": 169.949997
      },
      {
        "month": 11,
        "priceLow": 164.509995,
        "priceHigh": 176.710007
      },
      {
        "month": 12,
        "priceLow": 162.720001,
        "priceHigh": 179.179993
      }
    ]
  },
  {
    "year": 2020,
    "bilIcomePS": 9.25,
    "dividend": 5.88,
    "prices": [
      {
        "month": 1,
        "priceLow": 158.229996,
        "priceHigh": 182.550003
      },
      {
        "month": 2,
        "priceLow": 145.970001,
        "priceHigh": 165.039993
      },
      {
        "month": 3,
        "priceLow": 114.040001,
        "priceHigh": 154.740005
      },
      {
        "month": 4,
        "priceLow": 131.009995,
        "priceHigh": 163.080002
      },
      {
        "month": 5,
        "priceLow": 131.119995,
        "priceHigh": 159.869995
      },
      {
        "month": 6,
        "priceLow": 150.100006,
        "priceHigh": 169.539993
      },
      {
        "month": 7,
        "priceLow": 148.800003,
        "priceHigh": 163.380005
      },
      {
        "month": 8,
        "priceLow": 149.309998,
        "priceHigh": 167.490005
      },
      {
        "month": 9,
        "priceLow": 158.070007,
        "priceHigh": 173.199997
      },
      {
        "month": 10,
        "priceLow": 156.130005,
        "priceHigh": 173.190002
      },
      {
        "month": 11,
        "priceLow": 159.899994,
        "priceHigh": 179.630005
      },
      {
        "month": 12,
        "priceLow": 169.179993,
        "priceHigh": 177.460007
      }
    ]
  }
]
      `;
    const fvData = ref(JSON.parse(fvDataJson));
    //const fvData = ref([]);
    const fairValuesPerYear = ref({});
    //   const stockData = ref([]);
    const fairValueCalcTime = ref(10);

    const fairDivRenPerYear = ref({});

    const yearsToBeCalced = ref([]);

    // eslint-disable-next-line no-unused-vars
    const chart = ref({});

    return {
      fvData,
      fairValuesPerYear,
      fairValueCalcTime,
      fairDivRenPerYear,
      yearsToBeCalced,
    };
  },
  mounted() {
    this.calcFairValues();
    this.regenChartOption();
  },
  watch: {
    fairValueCalcTime() {
      this.calcFairValues();
      this.regenChartOption();
    },
  },
  methods: {
    changeFairValueCalcTime(newCalcTime) {
      this.fairValueCalcTime = newCalcTime;
      this.fairDivRenPerYear = {};
      this.fairValuesPerYear = {};
      this.yearsToBeCalced = [];
    },
    calcFairValues() {
      if (this.fvData.length > this.fairValueCalcTime) {
        let firstYear = this.fvData.map((x) => x.year).sort((a, b) => a - b)[0];
        let firstYearCalcable = firstYear + this.fairValueCalcTime;
        let lastYearCalcable = this.fvData
          .map((x) => x.year)
          .sort((a, b) => a - b)[this.fvData.length - 1];
        let kgvsPerYear = {};
        let kgvPerYear = {};
        let divRenPerYear = {};
        this.fvData.forEach((x) => {
          let kgvs = [];
          let priceSum = 0;
          x.prices.forEach((price) => {
            var aktKgv = this.calcKGVHighLow(
              x.bilIcomePS,
              price.priceLow,
              price.priceHigh
            );
            priceSum += price.priceLow + price.priceHigh;
            if (aktKgv > 0) {
              kgvs.push(aktKgv);
            }
          });
          priceSum = priceSum / (x.prices.length * 2);
          divRenPerYear[x.year.toString()] = x.dividend / priceSum;
          let avgPrice = this.calcAvgPrice(x.prices);
          kgvPerYear[x.year.toString()] = this.calcKGV(x.bilIcomePS, avgPrice);
          kgvsPerYear[x.year.toString()] = kgvs;
        });

        for (let i = firstYearCalcable; i < lastYearCalcable; i++) {
          let kgvsInAccount = [];
          let avgDiv = 0;
          this.yearsToBeCalced.push(i.toString());
          for (let j = i - this.fairValueCalcTime; j < i; j++) {
            kgvsPerYear[j.toString()].forEach((x) => kgvsInAccount.push(x));
            avgDiv += divRenPerYear[j];
            //kgvsInAccount.push(kgvPerYear[j.toString()]);
          }
          avgDiv = avgDiv / this.fairValueCalcTime;
          this.fairDivRenPerYear[i.toString()] =
            this.fvData.find((x) => x.year == i).dividend / avgDiv;
          kgvsInAccount.sort((a, b) => a - b);
          let median = this.calcMediaOfSorted(kgvsInAccount);
          let standardDeviation = this.getStandardDeviation(
            kgvsInAccount,
            median
          );
          kgvsInAccount = kgvsInAccount.filter(
            (x) =>
              x > median - standardDeviation * 3 ||
              x < median + standardDeviation * 3
          );
          this.fairValuesPerYear[i] =
            kgvsInAccount.reduce((a, b) => a + b, 0) / kgvsInAccount.length;

          this.fairValuesPerYear[i] =
            this.fairValuesPerYear[i] *
            this.fvData.find((x) => x.year == i).bilIcomePS;

          /*
          console.log("Jahr " + i + ":");
          console.log(kgvsInAccount);
          console.log(median);
          console.log(standardDeviation);
          */
          kgvsInAccount = [];
        }
      }
    },
    calcKGVHighLow(income, priceLow, priceHigh) {
      return (priceLow + priceHigh) / 2 / income;
    },
    calcKGV(income, price) {
      return price / income;
    },
    calcAvgPrice(prices) {
      let sum = 0;
      prices.forEach((x) => {
        sum += x.priceLow;
        sum += x.priceHigh;
      });
      return sum / (prices.length * 2);
    },
    calcMediaOfSorted(values) {
      let middle = Math.floor(values.length / 2);
      if (values % 2) {
        return values[middle];
      } else {
        return (values[middle - 1] + values[middle]) / 2.0;
      }
    },
    getStandardDeviation(values, mean) {
      let n = values.length;
      return Math.sqrt(
        values.map((x) => Math.pow(x - mean, 2)).reduce((a, b) => a + b) / n
      );
    },
    regenChartOption() {
      var color = "currentColor";
      var fvIcome = [];
      var stockData = [];
      var categories = [];
      var income = [];
      var fvDiv = [];
      var dividend = [];
      this.yearsToBeCalced.forEach((x) => {
        fvIcome.push([
          new Date(parseInt(x), 11, 31).getTime(),
          this.fairValuesPerYear[x],
        ]);
        fvDiv.push([
          new Date(parseInt(x), 11, 31).getTime(),
          this.fairDivRenPerYear[x],
        ]);
        //categories.push(parseInt(x));
      });
      console.log(this.fairDivRenPerYear);
      this.fvData.forEach((x) => {
        x.prices.forEach((y) => {
          stockData.push([
            new Date(x.year, y.month - 1, 1).getTime(),
            (y.priceLow + y.priceHigh) / 2,
          ]);
        });
        income.push([new Date(x.year, 11, 31).getTime(), x.bilIcomePS]);
        dividend.push([new Date(x.year, 11, 31).getTime(), x.dividend]);
      });
      var series = [
        {
          name: "Fair Value bil. Gewinn",
          data: fvIcome,
          type: "line",
        },
        {
          name: "Fair Value Dividende",
          data: fvDiv,
          type: "line",
        },
        {
          name: "Kurs",
          data: stockData,
          type: "area",
        },

        {
          name: "Gewinn",
          data: income,
          type: "area",
        },

        {
          name: "Dividende",
          data: dividend,
          type: "area",
        },
      ];
      var chartOptions = {
        chart: {
          vueBaseContext: this,
          type: "line",
          width: "100%",
          height: "500px",
          toolbar: {
            show: true,
            tools: {
              download: false,
              selection: false,
              zoom: false,
              zoomin: false,
              zoomout: false,
              pan: false,
              reset: false,
              customIcons: [
                {
                  icon: '<span class="custom-toolbar-icon custom-icon__10y mr-2 inline-block text-gray-800 dark:text-brand-white hover:underline text-base">1Y</span>',
                  click: () => {
                    this.changeFairValueCalcTime(1);
                  },
                },
                {
                  icon: '<span class="custom-toolbar-icon custom-icon__10y mr-2 inline-block text-gray-800 dark:text-brand-white hover:underline text-base">3Y</span>',
                  click: () => {
                    this.changeFairValueCalcTime(3);
                  },
                },
                {
                  icon: '<span class="custom-toolbar-icon custom-icon__10y mr-2 inline-block text-gray-800 dark:text-brand-white hover:underline text-base">5Y</span>',

                  click: () => {
                    this.changeFairValueCalcTime(5);
                  },
                },
                {
                  icon: '<span class="custom-toolbar-icon custom-icon__10y mr-2 inline-block text-gray-800 dark:text-brand-white hover:underline text-base">10Y</span>',
                  click: () => {
                    this.changeFairValueCalcTime(10);
                  },
                },
              ],
            },
          },
        },
        fill: {
          opacity: [1, 1, 0.1, 0.1, 0.1],
          gradient: {
            inverseColors: false,
            shade: "light",
            type: "vertical",
            opacityFrom: 0.85,
            opacityTo: 0.55,
            stops: [0, 100, 100, 100],
          },
        },
        colors: ["#e24158", "#a9cef2", "#67a3ff", "#eb8693", "#c5dcf2"],
        legend: {
          show: true,
          showForSingleSeries: true,
          labels: {
            colors: color,
          },
        },
        series: series,
        tooltip: {
          enabled: true,
        },
        dataLabels: {
          enabled: false,
        },
        stroke: {
          width: [2, 2, 2, 2, 2],
          curve: "smooth",
        },
        yaxis: [
          {
            seriesName: "Fair Value bil. Gewinn",

            labels: {
              style: {
                colors: color,
              },
              formatter: (value) => {
                return new Intl.NumberFormat("de-DE", {
                  style: "currency",
                  currency: "USD",
                }).format(value);
              },
            },
          },
          {
            seriesName: "Fair Value bil. Gewinn",
            show: false,
            labels: {
              style: {
                colors: color,
              },
              formatter: (value) => {
                return new Intl.NumberFormat("de-DE", {
                  style: "currency",
                  currency: "USD",
                }).format(value);
              },
            },
          },
          {
            seriesName: "Fair Value bil. Gewinn",
            show: false,
            labels: {
              style: {
                colors: color,
              },
              formatter: (value) => {
                return new Intl.NumberFormat("de-DE", {
                  style: "currency",
                  currency: "USD",
                }).format(value);
              },
            },
          },
          {
            seriesName: "Gewinn",
            opposite: true,
            labels: {
              style: {
                colors: color,
              },
              formatter: (value) => {
                return new Intl.NumberFormat("de-DE", {
                  style: "currency",
                  currency: "USD",
                }).format(value);
              },
            },
          },
          {
            seriesName: "Gewinn",
            show: false,
            labels: {
              style: {
                colors: color,
              },
              formatter: (value) => {
                return new Intl.NumberFormat("de-DE", {
                  style: "currency",
                  currency: "USD",
                }).format(value);
              },
            },
          },
        ],
        xaxis: {
          categories: categories,
          type: "datetime",
          labels: {
            style: {
              colors: color,
            },
          },
        },
      };
      if (!this.chart) {
        this.chart = new ApexCharts(
          document.querySelector("#chartplh"),
          chartOptions
        );
        this.chart.render();
      } else {
        this.chart.updateOptions(chartOptions);
        this.chart.updateSeries(series);
      }
    },
  },
};
</script>