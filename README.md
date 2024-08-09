# Accident_Analysis

## Accident
* with df_drop 
* X = all parameters except y (severity)
* Y = severity
* Y was not encoded
* Branch Neural Network
* 2 hidden layers
* shared_layer1 = layers.Dense(64, activation='relu')(input_layer)
* shared_layer2 = layers.Dense(32, activation='relu')(shared_layer1)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer2)
* Severity Accuracy: 0.3543262183666229

## Accident_2

* with df_drop
* Y was not encoded
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* Branch Neural Network Model
* 2 hidden layers
* shared_layer1 = layers.Dense(64, activation='relu')(input_layer)
* shared_layer2 = layers.Dense(32, activation='relu')(shared_layer1)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer2)
* Severity Accuracy: 0.35357803106307983

## Accident_3

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* OneHotEncoder Y
* Sequential Neural Network Model
* nn_model = tf.keras.models.Sequential()
* 2 hidden layers
* nn_model.add(tf.keras.layers.Dense(units=20, activation="relu", input_dim=X.shape[1]))
* nn_model.add(tf.keras.layers.Dense(units=10, activation="relu"))
*  with 5 output neurons
* nn_model.add(tf.keras.layers.Dense(units=5, activation="softmax"))
* Loss: 0.2950458228588104, Accuracy: 0.8717349171638489

## Accident_4

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* Categorize Y; df_drop['Severity'] = np.where(df_drop['Severity'].isin([0,1]),0,1)
* Branch neural network model
* 1 shared_layer
* shared_layer1 = layers.Dense(20, activation='relu')(input_layer)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer1)
* Severity Accuracy: 0.6853501200675964

## Accident_5

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* Categorie Y; df_drop['Severity'] = np.where(df_drop['Severity'].isin([0,1]),0,np.where(df_drop['Severity'].isin([3,4]),2,1))
* Branch neural network model
* 1 shared_layer
* shared_layer1 = layers.Dense(20, activation='relu')(input_layer)
* severity_output = layers.Dense(1, activation='sigmoid', name='severity_output')(shared_layer1)
* Severity Accuracy: 0.8696656227111816

## Accident_6

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* Categorie Y; df_drop['Severity'] = np.where(df_drop['Severity'].isin([0,1]),0,np.where(df_drop['Severity'].isin([3,4]),2,1))
* OneHotEcoder Y; 3 output neurons
* Sequential Neural Network Model
* nn_model = tf.keras.models.Sequential()
* 2 hidden layers
* nn_model.add(tf.keras.layers.Dense(units=20, activation="relu", input_dim=X.shape[1]))
* nn_model.add(tf.keras.layers.Dense(units=10, activation="relu"))
* nn_model.add(tf.keras.layers.Dense(units=3, activation="softmax"))
* Loss: 0.2950458228588104, Accuracy: 0.8717349171638489

## Accident_7

* with df_drop
* df_drop.corr(method="spearman")['Severity']
* df_drop_corr = df_drop.corr(method="spearman")['Severity']: Selected high 7 correlation parameters
* Categorie Y; df_drop['Severity'] = np.where(df_drop['Severity'].isin([0,1]),0,1)
* OneHotEcoder Y; 2 output neurons
* Sequential Neural Network Model
* nn_model = tf.keras.models.Sequential()
* 2 hidden layers
* nn_model.add(tf.keras.layers.Dense(units=20, activation="relu", input_dim=X.shape[1]))
* nn_model.add(tf.keras.layers.Dense(units=10, activation="relu"))
* nn_model.add(tf.keras.layers.Dense(units=2, activation="softmax"))
* Loss: 0.02754800207912922, Accuracy: 0.994331955909729
