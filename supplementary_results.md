# Supplementary Statistical Results

This file provides supplementary statistical results for **GNN-Enabled Robust Hybrid Precoding with Score-Based CSI Generation and Denoising**. The four tables correspond to Tables IV–VII in the response letter and support the discussion of statistical reliability in Comment 3.5.

## Reading the tables

- All sum rates are in **bit/s/Hz**; CSI estimation SNRs are in **dB**.
- `(K, N_T)` denotes the number of users and transmit antennas, respectively.
- NY, LA, and CHI denote New York, Los Angeles, and Chicago.
- Tables IV and V report **mean ± sample standard deviation** across three independent training and evaluation runs with seeds 40, 41, and 42. Sample standard deviation uses the denominator `n - 1`.
- Each value in Tables VI and VII is the test-set average sum rate for one run.
- ECRNet Refinement and Robust Training denote the corresponding DMP-GAT variants.
- Reported values are reproduced from the response letter at its displayed precision. Recomputing summary statistics from the rounded individual-run values can produce small differences in the last reported digit.

## Table IV. High-resolution CSI: mean and sample standard deviation

Mean achievable sum rates and standard deviations over three independent runs for representative methods in Table I of the manuscript.

<table>
  <thead>
    <tr>
      <th>(K, N<sub>T</sub>)</th>
      <th>City</th>
      <th>AO</th>
      <th>CensNet</th>
      <th>DMP-GAT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="3">(8,16)</td>
      <td align="center">NY</td>
      <td align="center">7.16 ± 0.53</td>
      <td align="center">11.28 ± 0.04</td>
      <td align="center">12.98 ± 0.05</td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">6.18 ± 0.65</td>
      <td align="center">17.90 ± 0.30</td>
      <td align="center">20.48 ± 0.19</td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">14.75 ± 0.86</td>
      <td align="center">14.59 ± 0.69</td>
      <td align="center">19.51 ± 0.53</td>
    </tr>
    <tr>
      <td align="center" rowspan="3">(16,32)</td>
      <td align="center">NY</td>
      <td align="center">11.94 ± 0.94</td>
      <td align="center">16.91 ± 0.07</td>
      <td align="center">18.78 ± 0.22</td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">13.50 ± 1.12</td>
      <td align="center">29.03 ± 0.57</td>
      <td align="center">37.61 ± 0.17</td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">31.39 ± 1.28</td>
      <td align="center">17.13 ± 0.41</td>
      <td align="center">32.86 ± 0.75</td>
    </tr>
  </tbody>
</table>

## Table V. Imperfect CSI: representative mean and sample standard deviation

Representative comparisons of DMP-GAT variants in Fig. 6 of the manuscript under high and low CSI estimation SNRs.

### (a) High-SNR comparisons

<table>
  <thead>
    <tr>
      <th rowspan="2">City</th>
      <th rowspan="2">(K, N<sub>T</sub>)</th>
      <th colspan="2">5 dB</th>
      <th colspan="2">10 dB</th>
    </tr>
    <tr>
      <th>DMP-GAT</th>
      <th>ECRNet<br>Refinement</th>
      <th>DMP-GAT</th>
      <th>ECRNet<br>Refinement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">NY</td>
      <td align="center">(8,16)</td>
      <td align="center">12.24 ± 0.20</td>
      <td align="center">12.95 ± 0.07</td>
      <td align="center">12.44 ± 0.10</td>
      <td align="center">12.88 ± 0.06</td>
    </tr>
    <tr>
      <td align="center">NY</td>
      <td align="center">(16,32)</td>
      <td align="center">17.75 ± 1.16</td>
      <td align="center">18.69 ± 0.79</td>
      <td align="center">18.50 ± 0.58</td>
      <td align="center">18.71 ± 0.05</td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">(8,16)</td>
      <td align="center">17.48 ± 0.10</td>
      <td align="center">19.98 ± 0.20</td>
      <td align="center">19.08 ± 0.20</td>
      <td align="center">20.06 ± 0.21</td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(8,16)</td>
      <td align="center">18.73 ± 0.44</td>
      <td align="center">19.60 ± 0.16</td>
      <td align="center">19.38 ± 0.13</td>
      <td align="center">19.54 ± 0.47</td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(16,32)</td>
      <td align="center">30.52 ± 0.50</td>
      <td align="center">32.91 ± 0.73</td>
      <td align="center">32.53 ± 0.67</td>
      <td align="center">32.82 ± 0.79</td>
    </tr>
  </tbody>
</table>

### (b) Low-SNR comparisons

<table>
  <thead>
    <tr>
      <th rowspan="2">City</th>
      <th rowspan="2">(K, N<sub>T</sub>)</th>
      <th colspan="2">−10 dB</th>
      <th colspan="2">−5 dB</th>
    </tr>
    <tr>
      <th>Robust<br>Training</th>
      <th>ECRNet<br>Refinement</th>
      <th>Robust<br>Training</th>
      <th>ECRNet<br>Refinement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">NY</td>
      <td align="center">(8,16)</td>
      <td align="center">10.17 ± 0.12</td>
      <td align="center">10.01 ± 0.06</td>
      <td align="center">11.21 ± 0.32</td>
      <td align="center">11.25 ± 0.07</td>
    </tr>
  </tbody>
</table>

## Table VI. High-resolution CSI: individual-run results

Individual-run sum rates for the methods compared in Table IV.

<table>
  <thead>
    <tr>
      <th rowspan="2">City</th>
      <th rowspan="2">(K, N<sub>T</sub>)</th>
      <th colspan="3">Seed 40</th>
      <th colspan="3">Seed 41</th>
      <th colspan="3">Seed 42</th>
    </tr>
    <tr>
      <th>AO</th>
      <th>CensNet</th>
      <th>DMP-GAT</th>
      <th>AO</th>
      <th>CensNet</th>
      <th>DMP-GAT</th>
      <th>AO</th>
      <th>CensNet</th>
      <th>DMP-GAT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">NY</td>
      <td align="center" rowspan="3">(8,16)</td>
      <td align="center">6.57</td>
      <td align="center">11.31</td>
      <td align="center"><strong>13.01</strong></td>
      <td align="center">7.31</td>
      <td align="center">11.30</td>
      <td align="center"><strong>12.92</strong></td>
      <td align="center">7.60</td>
      <td align="center">11.23</td>
      <td align="center"><strong>13.02</strong></td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">6.70</td>
      <td align="center">17.66</td>
      <td align="center"><strong>20.43</strong></td>
      <td align="center">5.45</td>
      <td align="center">17.81</td>
      <td align="center"><strong>20.32</strong></td>
      <td align="center">6.38</td>
      <td align="center">18.24</td>
      <td align="center"><strong>20.70</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">13.76</td>
      <td align="center">14.07</td>
      <td align="center"><strong>19.10</strong></td>
      <td align="center">15.22</td>
      <td align="center">15.37</td>
      <td align="center"><strong>19.32</strong></td>
      <td align="center">15.27</td>
      <td align="center">14.33</td>
      <td align="center"><strong>20.11</strong></td>
    </tr>
    <tr>
      <td align="center">NY</td>
      <td align="center" rowspan="3">(16,32)</td>
      <td align="center">12.67</td>
      <td align="center">16.99</td>
      <td align="center"><strong>18.59</strong></td>
      <td align="center">10.88</td>
      <td align="center">16.86</td>
      <td align="center"><strong>19.01</strong></td>
      <td align="center">12.28</td>
      <td align="center">16.88</td>
      <td align="center"><strong>18.73</strong></td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">12.57</td>
      <td align="center">29.28</td>
      <td align="center"><strong>37.41</strong></td>
      <td align="center">13.20</td>
      <td align="center">28.38</td>
      <td align="center"><strong>37.72</strong></td>
      <td align="center">14.74</td>
      <td align="center">29.44</td>
      <td align="center"><strong>37.71</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">31.50</td>
      <td align="center">17.24</td>
      <td align="center"><strong>32.83</strong></td>
      <td align="center">30.06</td>
      <td align="center">17.47</td>
      <td align="center"><strong>32.12</strong></td>
      <td align="center">32.62</td>
      <td align="center">16.68</td>
      <td align="center"><strong>33.62</strong></td>
    </tr>
  </tbody>
</table>

## Table VII. Imperfect CSI: individual-run results

Individual-run sum rates for the comparisons in Table V.

### (a) High-SNR comparisons

<table>
  <thead>
    <tr>
      <th rowspan="2">Seed</th>
      <th rowspan="2">City</th>
      <th rowspan="2">(K, N<sub>T</sub>)</th>
      <th colspan="2">5 dB</th>
      <th colspan="2">10 dB</th>
    </tr>
    <tr>
      <th>DMP-GAT</th>
      <th>ECRNet<br>Refinement</th>
      <th>DMP-GAT</th>
      <th>ECRNet<br>Refinement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="5">40</td>
      <td align="center">NY</td>
      <td align="center">(8,16)</td>
      <td align="center">12.19</td>
      <td align="center"><strong>12.95</strong></td>
      <td align="center">12.52</td>
      <td align="center"><strong>12.95</strong></td>
    </tr>
    <tr>
      <td align="center">NY</td>
      <td align="center">(16,32)</td>
      <td align="center">16.68</td>
      <td align="center"><strong>19.55</strong></td>
      <td align="center">18.27</td>
      <td align="center"><strong>18.73</strong></td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">(8,16)</td>
      <td align="center">17.57</td>
      <td align="center"><strong>20.20</strong></td>
      <td align="center">19.25</td>
      <td align="center"><strong>20.20</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(8,16)</td>
      <td align="center">18.70</td>
      <td align="center"><strong>19.43</strong></td>
      <td align="center"><strong>19.48</strong></td>
      <td align="center">19.01</td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(16,32)</td>
      <td align="center">30.00</td>
      <td align="center"><strong>32.53</strong></td>
      <td align="center">31.82</td>
      <td align="center"><strong>32.78</strong></td>
    </tr>
    <tr>
      <td align="center" rowspan="5">41</td>
      <td align="center">NY</td>
      <td align="center">(8,16)</td>
      <td align="center">12.45</td>
      <td align="center"><strong>13.02</strong></td>
      <td align="center">12.46</td>
      <td align="center"><strong>12.82</strong></td>
    </tr>
    <tr>
      <td align="center">NY</td>
      <td align="center">(16,32)</td>
      <td align="center"><strong>18.98</strong></td>
      <td align="center">17.99</td>
      <td align="center"><strong>19.15</strong></td>
      <td align="center">18.76</td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">(8,16)</td>
      <td align="center">17.49</td>
      <td align="center"><strong>19.82</strong></td>
      <td align="center">18.86</td>
      <td align="center"><strong>19.81</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(8,16)</td>
      <td align="center">18.31</td>
      <td align="center"><strong>19.64</strong></td>
      <td align="center">19.43</td>
      <td align="center"><strong>19.92</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(16,32)</td>
      <td align="center">31.00</td>
      <td align="center"><strong>32.45</strong></td>
      <td align="center"><strong>32.60</strong></td>
      <td align="center">32.04</td>
    </tr>
    <tr>
      <td align="center" rowspan="5">42</td>
      <td align="center">NY</td>
      <td align="center">(8,16)</td>
      <td align="center">12.06</td>
      <td align="center"><strong>12.88</strong></td>
      <td align="center">12.33</td>
      <td align="center"><strong>12.86</strong></td>
    </tr>
    <tr>
      <td align="center">NY</td>
      <td align="center">(16,32)</td>
      <td align="center">17.57</td>
      <td align="center"><strong>18.52</strong></td>
      <td align="center">18.07</td>
      <td align="center"><strong>18.65</strong></td>
    </tr>
    <tr>
      <td align="center">LA</td>
      <td align="center">(8,16)</td>
      <td align="center">17.37</td>
      <td align="center"><strong>19.91</strong></td>
      <td align="center">19.12</td>
      <td align="center"><strong>20.16</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(8,16)</td>
      <td align="center">19.19</td>
      <td align="center"><strong>19.74</strong></td>
      <td align="center">19.23</td>
      <td align="center"><strong>19.70</strong></td>
    </tr>
    <tr>
      <td align="center">CHI</td>
      <td align="center">(16,32)</td>
      <td align="center">30.56</td>
      <td align="center"><strong>33.75</strong></td>
      <td align="center">33.16</td>
      <td align="center"><strong>33.63</strong></td>
    </tr>
  </tbody>
</table>

### (b) Low-SNR comparisons: NY, (K, N<sub>T</sub>) = (8, 16)

<table>
  <thead>
    <tr>
      <th rowspan="2">Seed</th>
      <th colspan="2">−10 dB</th>
      <th colspan="2">−5 dB</th>
    </tr>
    <tr>
      <th>Robust<br>Training</th>
      <th>ECRNet<br>Refinement</th>
      <th>Robust<br>Training</th>
      <th>ECRNet<br>Refinement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">40</td>
      <td align="center"><strong>10.06</strong></td>
      <td align="center">10.00</td>
      <td align="center"><strong>11.57</strong></td>
      <td align="center">11.26</td>
    </tr>
    <tr>
      <td align="center">41</td>
      <td align="center"><strong>10.29</strong></td>
      <td align="center">10.08</td>
      <td align="center">11.01</td>
      <td align="center"><strong>11.32</strong></td>
    </tr>
    <tr>
      <td align="center">42</td>
      <td align="center"><strong>10.17</strong></td>
      <td align="center">9.96</td>
      <td align="center">11.03</td>
      <td align="center"><strong>11.17</strong></td>
    </tr>
  </tbody>
</table>
