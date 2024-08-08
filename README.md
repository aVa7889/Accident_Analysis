# Accident_Analysis

## Accident
* df_drop.corr(method="spearman")['Severity']
* X = all parameters except y (severity)
* Y = severity
* shared_layer1 = layers.Dense(64, activation='relu')(input_layer)
* shared_layer2 = layers.Dense(32, activation='relu')(shared_layer1)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer2)
* Severity Accuracy: 0.3543262183666229

## Accident_2



## Accident_3



## Accident_4


## Accident_5
