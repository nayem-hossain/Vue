# Understand Vue

## Options Vs Composition API Style

  Options API:
  
    This is the traditional way of writing Vue components.
    
    For Example:
        export default {
          data() {
            return {
              count: 0
            };
          },
          methods: {
            increment() {
              this.count++;
            }
          }
        };

    
  Composition API: 
  
    This is a newer addition to Vue.js that provides more flexibility and organization for larger and more complex components.

    For Example:
    import { reactive, computed } from 'vue';
    
    export default {
      setup() {
        const state = reactive({
          count: 0
        });
    
        const increment = () => {
          state.count++;
        };
    
        const doubleCount = computed(() => state.count * 2);
    
        return {
          state,
          increment,
          doubleCount
        };
      }
    };

  Comparison:

    Options API:
    
    Familiar and widely used.
    Easy to understand for beginners.
    Good for small to medium-sized components.
    All component options are contained within a single object.
    
    Composition API:
    
    Offers better organization and reusability, especially for larger and more complex components.
    Allows logic to be broken down into smaller, more manageable pieces.
    Encourages composition and separation of concerns.
    Can make code more readable and maintainable, especially as components grow in complexity.
