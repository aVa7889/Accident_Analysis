# Accident_Analysis

## Accident
* with df_drop 
* X = all parameters except y (severity)
* Y = severity
* shared_layer1 = layers.Dense(64, activation='relu')(input_layer)
* shared_layer2 = layers.Dense(32, activation='relu')(shared_layer1)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer2)
* Severity Accuracy: 0.3543262183666229

## Accident_2

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* shared_layer1 = layers.Dense(64, activation='relu')(input_layer)
* shared_layer2 = layers.Dense(32, activation='relu')(shared_layer1)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer2)
* Severity Accuracy: 0.35357803106307983

## Accident_3

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* OneHotEncoder Y
* Sequential model instance
* nn_model = tf.keras.models.Sequential()
* nn_model.add(tf.keras.layers.Dense(units=20, activation="relu", input_dim=X.shape[1]))
* nn_model.add(tf.keras.layers.Dense(units=10, activation="relu"))
*  with 5 output neurons
* nn_model.add(tf.keras.layers.Dense(units=5, activation="softmax"))
* Loss: 0.2950458228588104, Accuracy: 0.8717349171638489

## Accident_4


## Accident_5
