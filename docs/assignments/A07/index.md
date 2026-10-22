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
    
  <img width="740" height="670" alt="Screenshot 2026-10-15 104808" src="https://github.com/user-attachments/assets/500b4201-e15b-4daf-a109-e438ed59a96e" style="width: 30%; height: auto;"/>
    <img width="713" height="687" alt="Screenshot 2026-10-15 104943" src="https://github.com/user-attachments/assets/5753b4c9-d756-44f6-abd0-f26b3d4bce0b"  style="width: 30%; height: auto;"/>
    <img width="803" height="681" alt="Screenshot 2026-10-15 105012" src="https://github.com/user-attachments/assets/2bcea5c0-07d2-4ca3-900c-9e6454256fea" style="width: 30%; height: auto;"/>


  <h4>Mesh 2</h4>
  
  <img width="757" height="705" alt="Screenshot 2026-10-15 111600" src="https://github.com/user-attachments/assets/c97ca7d3-305f-4fc6-8345-d90a6b42338c"  style="width: 30%; height: auto;"/>
  <img width="760" height="666" alt="Screenshot 2026-10-15 111630" src="https://github.com/user-attachments/assets/461e7e80-caf1-4036-8ee8-bccf2706a332"   style="width: 30%; height: auto;"/>
    <img width="772" height="686" alt="Screenshot 2026-10-15 111650" src="https://github.com/user-attachments/assets/b2b1d804-72b8-431c-a0ca-eb9ed30aabc2" style="width: 30%; height: auto;"/>


  <h4>Mesh 3</h4>
  
  <img width="793" height="695" alt="Screenshot 2026-10-15 114430" src="https://github.com/user-attachments/assets/5d4d7d34-e6ef-4b7b-8f33-321ff3d6052a"  style="width: 30%; height: auto;"/>
    <img width="757" height="715" alt="Screenshot 2026-10-15 114507" src="https://github.com/user-attachments/assets/d52b21ef-a0ca-4e87-8965-a09462e44895"   style="width: 30%; height: auto;"/>
    <img width="795" height="738" alt="Screenshot 2026-10-15 114705" src="https://github.com/user-attachments/assets/30398517-1461-4cc7-853a-b537ba3524f1" style="width: 30%; height: auto;"/>


  
### Design 2

<h4>Mesh 1</h4>

  <img width="722" height="637" alt="Screenshot 2026-10-21 152257" src="https://github.com/user-attachments/assets/91e052a2-a2bd-4387-9879-c5a956f36834" style="width: 30%; height: auto;"/>
    <img width="661" height="617" alt="Screenshot 2026-10-21 152311" src="https://github.com/user-attachments/assets/c83b8324-9dc8-4303-839a-1ca6c053333a" style="width: 30%; height: auto;"/>
    <img width="727" height="607" alt="Screenshot 2026-10-21 152327" src="https://github.com/user-attachments/assets/f7320639-9e17-43a5-86d2-53b16b82335b" style="width: 30%; height: auto;"/>

  <h4>Mesh 2</h4>
  
  <img width="767" height="646" alt="Screenshot 2026-10-21 153027" src="https://github.com/user-attachments/assets/2bf92de1-15bd-4390-9c42-8657b7d96844" style="width: 30%; height: auto;"/>
    <img width="677" height="605" alt="Screenshot 2026-10-21 153040" src="https://github.com/user-attachments/assets/41c287c9-7d2f-4561-a420-bd6dbcd43db1" style="width: 30%; height: auto;"/>
    <img width="712" height="610" alt="Screenshot 2026-10-21 153012" src="https://github.com/user-attachments/assets/88635a81-7d64-4e22-9807-91b15f0d3865" style="width: 30%; height: auto;"/>

  <h4>Mesh 3</h4>
  
  <img width="802" height="615" alt="Screenshot 2026-10-21 154716" src="https://github.com/user-attachments/assets/0b914744-8777-4216-9e37-29b7e6c3d9ba" style="width: 30%; height: auto;"/>
    <img width="697" height="613" alt="Screenshot 2026-10-21 154727" src="https://github.com/user-attachments/assets/5fe87a29-37bb-480e-b3e9-87e66e72ca21" style="width: 30%; height: auto;"/>
    <img width="685" height="597" alt="Screenshot 2026-10-21 154737" src="https://github.com/user-attachments/assets/a97eb262-a8bf-4ca3-915e-3cb3151f71b5" style="width: 30%; height: auto;"/>


### Design 3
 
  <h4>Mesh 1</h4>
   
  <img width="802" height="615" alt="Screenshot 2026-10-21 154716" src="https://github.com/user-attachments/assets/f5041fc5-ada4-440c-8dba-161de01b5809" style="width: 30%; height: auto;"/>
    <img width="697" height="613" alt="Screenshot 2026-10-21 154727" src="https://github.com/user-attachments/assets/e76c7e2e-f348-4397-a102-1965a8c015bf" style="width: 30%; height: auto;"/>
    <img width="685" height="597" alt="Screenshot 2026-10-21 154737" src="https://github.com/user-attachments/assets/a6a8f220-ede6-46b6-9773-a46f46c0574a" style="width: 30%; height: auto;"/>

  <h4>Mesh 2</h4>
  
  <img width="725" height="656" alt="Screenshot 2026-10-21 182353" src="https://github.com/user-attachments/assets/41d1deb1-dda2-42b3-8562-b91dc7054c47" style="width: 30%; height: auto;"/>
    <img width="713" height="682" alt="Screenshot 2026-10-21 182406" src="https://github.com/user-attachments/assets/d9e93490-717b-432a-ae61-5a803d948976" style="width: 30%; height: auto;"/>
    <img width="692" height="686" alt="Screenshot 2026-10-21 182417" src="https://github.com/user-attachments/assets/7d978008-96d9-4a44-a8e4-95611c6fbfa7" style="width: 30%; height: auto;"/>

  
  <h4>Mesh 3</h4>
    
  <img width="732" height="673" alt="Screenshot 2026-10-21 182539" src="https://github.com/user-attachments/assets/92dc93bf-cda2-41a5-b8ce-716247bcb88b" style="width: 30%; height: auto;"/>
    <img width="683" height="647" alt="Screenshot 2026-10-21 182807" src="https://github.com/user-attachments/assets/4269b6ad-a679-4885-ae1d-6942a7478361" style="width: 30%; height: auto;"/>
    <img width="670" height="657" alt="Screenshot 2026-10-21 182816" src="https://github.com/user-attachments/assets/16d1cdcd-12c8-4101-8e31-e4dde080063e" style="width: 30%; height: auto;"/>


### Design 4
  
<h4>Mesh 1</h4>
    
  <img width="771" height="677" alt="Screenshot 2026-10-21 195634" src="https://github.com/user-attachments/assets/4efb7b8f-91ed-40b1-9194-e4674e8d1f4c" style="width: 30%; height: auto;"/>
    <img width="738" height="620" alt="Screenshot 2026-10-21 195644" src="https://github.com/user-attachments/assets/e86515d8-c3f5-4594-86cd-514b50335f1d" style="width: 30%; height: auto;"/>
    <img width="782" height="622" alt="Screenshot 2026-10-21 195654" src="https://github.com/user-attachments/assets/555ad7ef-cbdb-45db-938a-9cbda1a7336b" style="width: 30%; height: auto;"/>

  <h4>Mesh 2</h4>
    
  <img width="672" height="530" alt="Screenshot 2026-10-21 204138" src="https://github.com/user-attachments/assets/918bccca-3295-4d4f-8aa6-e40e7fa127c1" style="width: 30%; height: auto;"/>
    <img width="655" height="560" alt="Screenshot 2026-10-21 204151" src="https://github.com/user-attachments/assets/6f9e76f0-b8ed-407e-a88a-2f00a38a5e65" style="width: 30%; height: auto;"/>
    <img width="642" height="532" alt="Screenshot 2026-10-21 204201" src="https://github.com/user-attachments/assets/072c456f-69bf-4878-a9b8-cf77b5296804" style="width: 30%; height: auto;"/>

  <h4>Mesh 3</h4>
    
<img width="735" height="622" alt="Screenshot 2026-10-21 195856" src="https://github.com/user-attachments/assets/46010f59-39ff-42e7-b782-ce6228344426" style="width: 30%; height: auto;"/>
    
  <img width="693" height="586" alt="Screenshot 2026-10-21 195904" src="https://github.com/user-attachments/assets/df9cf814-fe0c-4b25-a9b1-104e2749d94a" style="width: 30%; height: auto;"/>
    <img width="752" height="663" alt="Screenshot 2026-10-21 195917" src="https://github.com/user-attachments/assets/6ee4a870-c781-4689-8a05-dca3cf4a9e52" style="width: 30%; height: auto;"/>


### Link

  <h4>Mesh 1</h4>

  <img width="576" height="707" alt="Screenshot 2026-10-21 210648" src="https://github.com/user-attachments/assets/6733d428-9e44-4241-b3f4-9e83517d8ec0" style="width: 30%; height: auto;"/>
    <img width="478" height="692" alt="Screenshot 2026-10-21 210658" src="https://github.com/user-attachments/assets/373d4d1f-be49-4dc6-981d-065f7b865734" style="width: 30%; height: auto;"/>
    <img width="537" height="671" alt="Screenshot 2026-10-21 210712" src="https://github.com/user-attachments/assets/b4117d99-a652-44da-9e07-03d002f8d419" style="width: 30%; height: auto;"/>

  
  <h4>Mesh 2</h4>
  
<img width="535" height="681" alt="Screenshot 2026-10-21 210856" src="https://github.com/user-attachments/assets/f0b2256f-22bc-4b34-aa3b-4aea89de73b7" style="width: 30%; height: auto;"/>
    <img width="515" height="702" alt="Screenshot 2026-10-21 210922" src="https://github.com/user-attachments/assets/c4e71cab-923b-459b-87b1-43f452d10a58" style="width: 30%; height: auto;"/>
    <img width="523" height="687" alt="Screenshot 2026-10-21 210955" src="https://github.com/user-attachments/assets/2dedc7fc-103e-4090-b109-b8d68a929e13" style="width: 30%; height: auto;"/>

  
  <h4>Mesh 3</h4>
    
  <img width="586" height="710" alt="Screenshot 2026-10-21 220545" src="https://github.com/user-attachments/assets/f99e6ed6-8217-4707-ac38-29ebf08d2a7f" style="width: 30%; height: auto;"/>
    <img width="545" height="702" alt="Screenshot 2026-10-21 220533" src="https://github.com/user-attachments/assets/0a1885a7-6027-49ca-a1ef-19cf10637026" style="width: 30%; height: auto;"/>
    <img width="548" height="691" alt="Screenshot 2026-10-21 220523" src="https://github.com/user-attachments/assets/0abc71a3-a6b5-41d5-b8bb-188db580261f" style="width: 30%; height: auto;"/>


  
  <br>  <br>
