# Router State Transition Events
## $stateChangeStart
* Fires when state change transition begins.
* Use `event.preventDefault()` to prevent the transition from occuring.
```
$rootScope.$on('$stateChangeStart',
                function(event, toState, toParams, fromState, fromParams, options){
                    ...
                }
);
```
## $stateChangeSuccess
* Fired once the state transition is complete.
```
$rootScope.$on('$stateChangeSuccess',
                function(event, toState, toParams, fromState, fromParams){
                    ...
                }
);
```
## $stateChangeError
* Fires when an error occurs during transition.
```
$rootScope.$on('$stateChangeError',
                function(event, toState, toParams, fromState, fromParams, error){
                    ...
                }
);
```

