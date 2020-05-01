# data
# DON'T_CHANGE_THIS_CODE. It is used to let you check the result is correct 

X_train= [[0, 0], [0, 1], [1, 0], [1, 1]]
y_train=[0, 0, 0, 1]
# X_train, X_test, y_train, y_test=  X[:300],X[300:],y[:300], y[300:]
print ('X_train.shape= ',X_train.shape)
print ('y_train.shape= ',y_train.shape)
# print ('X_train= \n{}'.format (X_train[:5,:]))
lin_reg = Linear_Regression(alpha= 0.01, verbose=0, eps=1e-8)
lin_reg.fit (X_train, y_train)
lin_reg.draw_cost_changes()
# print ('R2 Score =', lin_reg.score(X_test, y_test))
print ('b: {}, w= {}'.format(lin_reg.intercept_, lin_reg.coef_))
print ('Normal Score =',lin_reg.normal(X, y))
