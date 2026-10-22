# A7 – FEA on Bracket

## Objective
The objective was to run a FEA on the bracket made for a T beam previously designed in A5 and A6. The purpose is to analyze and make iterative adjustments to make the bracket more stable. The bracket material is Ti-6Al-v4 with a load of 2F = 1200 Lbf. The goal is to converge on a 7% difference for the component results.

## Analyze

The initial design was the same one created in A6. One thing that I will note is that for one dimension, I entered incorrectly a smaller value than intended which had a small impact however it wouldn't prevent the part from failing in the slightest.
  <br>
<table>
  <thead>
    <tr>
      <th>Design 1</th>
      <th>Mesh1</th>
      <th>Mesh 2</th>
      <th>Mesh 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Max Stress</td>
      <td>1.2 E2 Ksi</td>
      <td>8.417 E2 Ksi</td>
      <td>1.033 E3 Ksi</td>
    </tr>
    <tr>
      <td>Max Deflection</td>
      <td>0.9667 in</td>
      <td>0.9947 in</td>
      <td>1.001 in</td>
    </tr>
    <tr>
      <td>S.F.</td>
      <td>0.1856</td>
      <td>0.1426</td>
      <td>0.1162</td>
    </tr>

  </tbody>
</table>

These results were catastrophic as the factor of safety was below 1 meaning that the part would fail. The yield stress being 1.2 E2 Ksi one would see that the max stress grew catastrophically as the mesh increased in detail. 
  <br> 
  <br>
What's the second design I managed to get above the safety factor for the first mesh however, as the mesh got finer the max stress increased over the yield stres

<table>
  <thead>
    <tr>
      <th>Design 2</th>
      <th>Mesh1</th>
      <th>Mesh 2</th>
      <th>Mesh 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Max Stress</td>
      <td>1.109 E2 Ksi</td>
      <td>1.561 E2 Ksi</td>
      <td>1.866 E2 Ksi</td>
    </tr>
    <tr>
      <td>Max Deflection</td>
      <td>0.1008 in</td>
      <td>0.1070 in</td>
      <td>0.1068 in</td>
    </tr>
    <tr>
      <td>S.F.</td>
      <td>1.082</td>
      <td>0.7689</td>
      <td>0.6431</td>
    </tr>
  </tbody>
</table>


<table>
  <thead>
    <tr>
      <th>Design 3</th>
      <th>Mesh1</th>
      <th>Mesh 2</th>
      <th>Mesh 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Max Stress</td>
      <td>1.033 E2 Ksi</td>
      <td>1.204 E2 Ksi</td>
      <td>1.246 E2 Ksi</td>
    </tr>
    <tr>
      <td>Max Deflection</td>
      <td>0.0.0722 in</td>
      <td>0.0763 in</td>
      <td>0.0769 in</td>
    </tr>
    <tr>
      <td>S.F.</td>
      <td>1.162</td>
      <td>0.997</td>
      <td>0.964</td>
    </tr>
  </tbody>
</table>




## Decide


## Communicate

