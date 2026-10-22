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
 <tfoot>
    <tr>
      <td colspan="2" style="text-align: center; font-weight: bold; background-color: #f9f9f9;">
        Weight: 0.1428 Lb
      </td>
    </tr>
  </tfoot>
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
 <tfoot>
    <tr>
      <td colspan="2" style="text-align: center; font-weight: bold; background-color: #f9f9f9;">
        Weight: 0.1699 Lb
      </td>
    </tr>
  </tfoot>
  </tbody>
</table>
  <br>
The third design managed to get even closer with the safety factor staying around one and also managed to decrease the deflection. The main problem that I once again ran into was the max dress increasing with the mesh growing finer.
  <br>

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
 <tfoot>
    <tr>
      <td colspan="2" style="text-align: center; font-weight: bold; background-color: #f9f9f9;">
        Weight: 0.1774 Lb
      </td>
    </tr>
  </tfoot>
  </tbody>
</table>
  <br>
  
With my final design I managed to achieve a safety factor above one with minimal change.
<table>
  <thead>
    <tr>
      <th>Design 4</th>
      <th>Mesh1</th>
      <th>Mesh 2</th>
      <th>Mesh 3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Max Stress</td>
      <td>77.67 Ksi</td>
      <td>92.09 Ksi</td>
      <td>96.42 Ksi</td>
    </tr>
    <tr>
      <td>Max Deflection</td>
      <td>0.0.0568 in</td>
      <td>0.0601 in</td>
      <td>0.0607 in</td>
    </tr>
    <tr>
      <td>S.F.</td>
      <td>1.545</td>
      <td>1.303</td>
      <td>1.245</td>
    </tr>
 <tfoot>
    <tr>
      <td colspan="2" style="text-align: center; font-weight: bold; background-color: #f9f9f9;">
        Weight: 0.1836 Lb
      </td>
    </tr>
  </tfoot>
  </tbody>
</table>




## Communicate
This assignment took longer than expected as I ran too many technical difficulties has my laptop had trouble rendering the messages in the beginning after some restarting and messing around. I managed to get it stable where I can make a simulation in a 30 seconds rather than 15 minutes. Even without these technical difficulties, I had misunderstood the safety factor as for some reason I didn't take accounts that it was dependent on the stress. Because of this, I went through trial and error for about an hour only to realize how much more simple it could've been.

## 2157

With the analysis of the link, one thing I found interesting was that the medium mesh was somehow larger when it came to max stress and smaller when it came to deflection than both the fine and large mesh.
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
      <td>8.858 Ksi</td>
      <td>8.979 Ksi</td>
      <td>8.942 Ksi</td>
    </tr>
    <tr>
      <td>Max Deflection</td>
      <td>0.00077 in</td>
      <td>0.000736 in</td>
      <td>0.00074 in</td>
    </tr>
    <tr>
      <td>S.F.</td>
      <td>13.55</td>
      <td>13.36</td>
      <td>13.42</td>
    </tr>
 <tfoot>
    <tr>
      <td colspan="2" style="text-align: center; font-weight: bold; background-color: #f9f9f9;">
        Weight: 0.0872 Lb
      </td>
    </tr>
  </tfoot>
  </tbody>
</table>

## Images

### Design 1
  <h4>Mesh 1</h4>
    <img width="740" height="670" alt="Screenshot 2026-10-15 104808" src="https://github.com/user-attachments/assets/500b4201-e15b-4daf-a109-e438ed59a96e" />
    <img width="713" height="687" alt="Screenshot 2026-10-15 104943" src="https://github.com/user-attachments/assets/5753b4c9-d756-44f6-abd0-f26b3d4bce0b" />

  <h4>Mesh 2</h4>
    <img width="757" height="705" alt="Screenshot 2026-10-15 111600" src="https://github.com/user-attachments/assets/c97ca7d3-305f-4fc6-8345-d90a6b42338c" />
    <img width="760" height="666" alt="Screenshot 2026-10-15 111630" src="https://github.com/user-attachments/assets/461e7e80-caf1-4036-8ee8-bccf2706a332" />

  <h4>Mesh 3</h4>
    <img width="793" height="695" alt="Screenshot 2026-10-15 114430" src="https://github.com/user-attachments/assets/5d4d7d34-e6ef-4b7b-8f33-321ff3d6052a" />
    <img width="757" height="715" alt="Screenshot 2026-10-15 114507" src="https://github.com/user-attachments/assets/d52b21ef-a0ca-4e87-8965-a09462e44895" />

  
### Design 2
  <h4>Mesh 1</h4>
  
  <h4>Mesh 2</h4>
  
  <h4>Mesh 3</h4>

### Design 3
  <h4>Mesh 1</h4>
  
  <h4>Mesh 2</h4>
  
  <h4>Mesh 3</h4>

### Design 4
  <h4>Mesh 1</h4>
  
  <h4>Mesh 2</h4>
  
  <h4>Mesh 3</h4>

### Link
  <h4>Mesh 1</h4>
  
  <h4>Mesh 2</h4>
  
  <h4>Mesh 3</h4>
