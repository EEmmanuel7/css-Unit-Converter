             //this is version 2 - improved 

            /**
             * Enhanced CSS unit converter with more accurate calculations
             * @param {number|string} value - Value to convert (with or without unit)
             * @param {string} toUnit - Target unit
             * @param {object} [options] - Conversion options
             * @param {string} [options.fromUnit] - Source unit if not in value
             * @param {number} [options.baseFontSize=16] - Base for rem (in px)
             * @param {HTMLElement} [options.contextElement] - For em/% conversions
             * @param {string} [options.property] - CSS property being converted (for %)
             * @param {number} [options.dpi=96] - Device pixels per inch
             * @return {number|string} - Converted value
             */

            /*
             * Author : Ezechias Emmanuel
             * contact : ezechias dot emmanuel at gmail dot com
             * License : MIT
             */

            // Basic conversions
            
            convertCSSUnit('16px', 'rem'); // "1rem" (with default 16px base)
            convertCSSUnit('1in', 'cm'); // "2.54cm"
            
            // With options
            convertCSSUnit(2, 'px', { fromUnit: 'cm' }); // "75.59055118110236px"
            convertCSSUnit('2em', 'px', { contextElement: document.body }); // Converts based on body's font size
            
            // Get numeric value only
            convertCSSUnit('16px', false); // Returns 16 (number)
