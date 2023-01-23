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
***
#### _Summary_
* ui-router exposes numerous state change events that our code is able to listen for.
* All ui-router events are fired on the $rootScope.
* $stateChangeStart - starts the state transition. Call `event.preventDefault()` to prevent the transition.
* $stateChangeSuccess indicates a successful transition end.
* $stateChangeError indicates that the transition failed, including having errors in the resolve. Listen for this event to catch ALL errors during state changes.
***